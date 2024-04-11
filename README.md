# Hello World in Go in Snap

This repo shows a minimal example of how to package a Go program in a Snap package.

## Standard Go build

`go build`

This should create a binary in the current directory called `helloworld`.
You can execute it as usual with:

```
$ ./helloworld 
hello world
```

## Snap build

To compile the Go code and put it inside a snap, run:

`snapcraft -v`

The output will look similar to this:

```
Starting Snapcraft X.X.X
...
Created snap package go-hello-world_0.1_amd64.snap
```

In the current directory there should now be a new file called `go-hello-world_0.1_amd64.snap`.

Install the snap by running:

`snap install ./go-hello-world_0.1_amd64.snap --dangerous --devmode`

Run the snap by calling its name. It should print out "hello world"

```
$ go-hello-world 
hello world
```

To clean up, remove the Snap from your system byt running:  
```
$ snap remove go-hello-world 
go-hello-world removed
```

> Note: Snap asks for your password when installing and removing packages.