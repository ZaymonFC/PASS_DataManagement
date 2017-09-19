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


