all: run-sizeof

clean:
	rm -f bin/run-sizeof

bin:
	mkdir bin

run-sizeof: run-sizeof.c bin
	gcc -o bin/run-sizeof run-sizeof.c -Wall
