# Learning Go
Repo for learning golang

## Installing Go
Go to https://golang.org/dl/

Select appropriate OS and download the installer.
Start the installer and follow the install steps to install the Go tools.

To validated it installed try the command `go version`
and it should display the current version installed `go version go1.12.5 darwin/amd64`.

## go CLI
`go build` - Compiles a bunch of go source code files
`go run` - Compiles and executes one or two files
`go fmt` - Formats all code in each file in the current directory
`go install` - Compiles and installs a package
`go get` - Downloads the raw source code of someone else's package
`go test` - Runs any tests associated with the current project

## main.go
How do you run the code in our project?

`go run main.go`

What does `package main` mean?

Package == Project == Workspace
A package is a collection of source code files. Its used to group together code with a similar purpose.

There are two types of packages:
* Executable - Generates a file we can run, an executable file.
* Reusable - Code used as 'helpers'. Good place to put reusable logic.

How do you know what type of package?

The name of the package that you use determines if you are making and executable or dependancy type package.
A `main` package name creates an executable type package.

`package main` defines a package that can be compile and executed. It must have `func` called `main`.

If any other name was choosen, when running `go build` it would compile nothing. It defines a package that can be used as a dependancy (helper code)

What does `import "fmt"` mean?

`import` form link to package you want to use.

`fmt` - standard library package that include with go by default. Short for 'format'.

List of standard package included with go - 
https://golang.org/pkg

What's the `func` thing?

`func` is a function!

How is the `main.go` file organized?

1st Package declartion - `package main`
2nd Import other pacakge that we need - `import "fmt"`
3rd Declare functions, tell Go to do things - 
``` 
func main() {
  fmt.Println("hi there")
}
```