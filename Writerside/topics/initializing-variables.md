# Initiliazing Variables

## Declaring Variables in Go

In Go, you can declare variables using either the `var` keyword or the short 
variable declaration `:=`.

### Using the 'var' keyword

You can declare a variable using the `var` keyword, where you specify the
variable name, data type, and optionally an initial value.

```Go
var age int
var name string = "John"
```

> If you don't provide an initial value, Go assigns the zero value for the 
> data type (e.g. 0 for numeric types, an empty string for strings, false 
> for boolean types)

### Using the Short Variable Declaration

Inside functions (only), you can use the short variable declaration := to 
declare and initialize variables. Go infers the data type from the assigned 
value.

```Go
age := 30
name := "John"
height := int(30) // Explicit Data Type Declaration
```

You can explicitly declare the data type of variable even when using the
short variable declaration :=. This can be useful when you want to be
explicit about the data type

> Short Variable Declaration `:=` can only be used inside Functions.
>
{ style="note" }

### Same Line Declarations

We are able to declare multiple variables

```Go
name, age := "Adam", 24
```

### Using 'var' for Multiple Variables

You can declare multiple variables in a single var statement, separating 
them with commas.

```Go
var (
   x int
   y float64
   z string
)
```

> Remember that Go promotes the use of short, meaningful variable names for better code 
> readability.