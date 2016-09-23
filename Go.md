# Installation(Ubuntu 16, 64x)

	$ wget https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz
	$ tar xvf go1.6.2.linux-amd64.tar.gz 
	$ sudo chown -R root:root ./go
	$ sudo mv go /usr/local

	$ vim ~/.bashrc or subl ~/.bashrc

**Add these lines**

	$ export GOPATH=$HOME/go-works
	$ export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin

	$ source ~/.bashrc

**Test**
	
	$ go

## Hello World

`hello-world.go`

	package main
	import "fmt"
	func main() {
	    fmt.Println("hello world")
	}

**Run**
	
	$ go run hello-world.go
	//=> hello world

**Build**
	
	$ go build hello-world.go
	$ ls
	// => hello-world hello-world.go
	$ ./hello-world
	//=> hello world
