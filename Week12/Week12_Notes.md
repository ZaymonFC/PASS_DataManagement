# Week 12 Notes

### Transaction
> A series of actions or operations carried out by a user of application which reads or changes contents of the database.
- The actions must be considered a logical unit of work on the DB
- Actions are either read(X) or write(X). Where read is reading X into memory and write is writing X into the DB
- An application program is a series of transactions with non DB processing in between

### Transaction Outcome
- Success, transaction commits and database reaches a new consistent state.
- Failure, transaction aborts and all changes are rolled back to revert the DB to a consistent state.

### ACID Properties of Transactions
- Atomicity | All or none. The actions in a transaction must be all completed otherwise all will be rolled back
- Consistency | The DB must go from one consistent state to another
- Isolation | Partial effects of uncommitted transactions should not interfere with other transactions
- Durability | Effects of committed transactions are permanent and must not be lost because of later failure

### Concurrency Control
- Concurrency control refers to managing the concurrently executing transactions, so that they do not interfere with each other.
> Multiple transactions running at the same time need to be controlled in a way to stop them interfering with each other.
- Serializability and recoverability can be ensured by concurrency control protocols.
    - A common control technique is called locking

### The Schedule
Concurrency Control problems can be avoided by __scheduling__ the read/write actions appropriately.
- The Schedule is the ordering of operations involving a set of transactions

### Serial Schedule
> Is a schedule where the operations of one transactions are complete before the actions of another.
This means that the concurrency of transactions is limited.

### Serializable Schedule
The schedule is not a serial schedule but all DB operations are ordered in such a way where the end result is the same as a serial schedule.
This concept is called a serializable schedule.
> These schedules ensure consistency as long as all transactions are able to commit.

### Locking
- Transaction uses locks to deny access to other transactions
- Generally a transaction must claim a shared (read) or exclusive (write) lock on a data item.
> Prevents other transaction from modifying an item or even reading it in the case of a write lock
- If a transaction has a shared lock, many transactions can read the value
- If a transaction has an exclusive lock, only that transaction and both read and write that data item
> These basic rules don't guarantee serializability.
> Learning about strict 2-phase locking is optional

### Dead Locks | Like a Mexican Standoff
A dead lock occurs when two or more transactions are waiting on each others 
Preventing deadlocks is difficult and requires looking into the future and never allowing deadlocks to occur
- Detection and recovery is more popular and easier to implement
    - When deadlock occurs abort on victim transaction (restarted after DL resolved)
- To check for deadlocks the system uses a timeout timer on each transaction

### Isolation Levels
The ANSI defines 4 isolation levels
1. READ UNCOMMITED | Permits a transaction to read rows that have not yet been committed
2. READ COMMITTED | Only committed rows can be seen by transactions
3. REPEATABLE READ | No changes made by other sessions since the transaction commenced
4. SERIALIZABE | Every transaction is completely isolated so that transactions act as if they were run one at a time

### The Types of Failures
- Catastrophic Failures
    - Use backup copy to restore past copy
    - Redo committed transactions since last backup
- Non-catastrophic failure
    - Identify changes which lead to inconsistency
    - Redo committed transactions
    - Undo aborted transactions


