shell: main.o listing.o misc.o time.o calc.o
			cc -o shell.exe -g main.o listing.o time.o calc.o
main.o: main.c common.h
	cc -c -g main.c
listing.o: listing.c common.h
	cc -c -g listing.c
misc.o: misc.c common.h
	cc -c -g misc.c
calc.o: calc.c common.h
	cc -c -g calc.c
time.o: time.c common.h
	cc -c -g time.c
clean:
	rm shell main.o listing.o calc.o time.o misc.o