# Hello World in Go

```go
package main

import "fmt"

func main() {
// Single-line comments start with "//".
// Comments are for documentation purposes and do not execute.
fmt.Println("Hello, world!")
}
```

## Breaking Down the Code

```go
package main
```
- Every file of 'Go' code has a `package` declaration at the top.
- A `package` in 'Go' is a way to organize and group related Go source code 
  files together. It provides a namespace for the code within it.
- Here, the `package` is referred to as main - as it builds into an 
  executable 'Go' program, that is, we can run this program standalone. It 
  acts as the main entry point for the program.

```go
import fmt
```
- The `import` statement in Go is used to include code from other packages 
  into your program. It allows you to use functions, types, and variables 
  defined in other packages.
- When you `import` a package, you make its code accessible in your Go
  source file.
- You can `import` multiple packages in a single Go source file. 
- Here, we `import` the `fmt` package from the standard library. We are 
  importing it because we make use of it in the `main` function.

```go
func main() { }
```
- The `main` function is the entry point to the program. 
- Every 'Go' program starts execution at the top of the 'main' function.
- When the `main` function finishes executing, your program exits

```go
fmt.Println("hello world")
```
This piece of code makes use of the 'fmt' package to print the string
'hello world!' to the console with the help of the `Println()` function that 
is exposed by this library.
