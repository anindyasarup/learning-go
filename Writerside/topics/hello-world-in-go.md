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
Every file of 'Go' code has a package declaration at the top. Here, the
package is referred to as main - as it builds into an executable 'Go'
program, that is, we can run this program standalone.

```go
import fmt
```
Here, we import the 'fmt' package from the standard library. We are
importing it because we make use of it in the 'main' function.

```go
func main() { }
```
The 'main' function is the entry point to the program. Every 'Go'
program starts execution at the top of the 'main' function.

```go
fmt.Println("hello world")
```
This piece of code makes use of the 'fmt' package to print the string
'hello world!' to the console with the help of the `Println()` function that is exposed by this library.
