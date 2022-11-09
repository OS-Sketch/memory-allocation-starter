all: run-sizeof

clean:
	rm -f bin/run-sizeof

bin:
	mkdir bin

run-sizeof: run-sizeof.go bin
	go build --o bin run-sizeof.go
