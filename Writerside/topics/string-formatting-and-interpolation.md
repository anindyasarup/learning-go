# String Formatting and Interpolation

String formatting and interpolation are essential techniques in Go for 
manipulating and displaying text. <br/>
Whether you want to create formatted output, embed variables in strings, or 
control how values are represented, Go provides powerful tools to achieve 
these tasks.

> Personally, I find the string formatting in Go to be inelegant/dated in 
> comparison to what you can achieve in interpreted languages like Python or 
> JavaScript and even C# 6.0 +!

## String Formatting

String formatting in Go is the process of specifying how values should be 
represented when converted to strings. It allows you to control the 
appearance of values in the output string. <br/> <br/> 
This is often used with the `fmt.Printf()` family of functions, which use 
format specifiers to define how data is presented.

### Basic String Formatting

The `%` character in Go is used as a format specifier in combination with the 
`fmt` package to control the formatting of values in strings

The `%v` format specifier prints a Go-syntax representation of a value. It's a 
versatile option when you're uncertain about which format specifier to use.

```Go
age := 30
s := fmt.Sprintf("I am %v years old", age) // I am 30 years old

s := fmt.Sprintf("I am %v years old", "way too many") // I am way too many years old

name := "Alice"
fmt.Printf("Name: %s, Age: %d\n", name, age) // Name: Alice, Age: 30
```

- `%s`: Formats a value as a string.
- `%d`: Formats an integer value.
- `%f`: Formats a floating-point value.
- `%x`: Formats an integer as a hexadecimal number.
- `%t`: Formats a boolean value.
- `%c`: Formats a single character.
- `%p`: Formats a pointer.

### Formatting Options
Go provides various formatting options, including width, precision, and 
alignment, zero-padding to tailor the appearance of your data when it's 
converted to strings.

```Go
// width formatting
width, num := 8, 42
fmt.Printf("|%*d|\n", width, num) // |      42|

// zero padding
fmt.Printf("|%05d|\n", num) // |0042|

// precision formatting
value := 3.14159
fmt.Printf("|%.2f|\n", value) // |3.14|
```

## String Interpolation

String interpolation is the act of embedding variables or expressions within 
a string to create a new string. In Go, you can use `fmt.Sprintf()` or raw 
string literals to perform string interpolation.

> The format specifiers used in both `fmt.Printf()` and `fmt.Sprintf()` are 
> the same.
> 
 {style="note"}

### Using 'fmt.Sprintf()'

```Go
name := "Anindya"
age := 26
greeting := fmt.Sprintf("Hello, my name is %s and I'm %d years old.", name, age)
// greeting -> Hello, my name is Anindya and I'm 26 years old.
```

### Raw String Literals

Raw string literals (enclosed in backticks) are another way to perform 
string interpolation in Go. They allow you to embed variables without the 
need for escape sequences.

```Go
name := "Toon"
age := 24
message := `Hello, my name is ` + name + ` and I'm ` + strconv.Itoa(age) + ` years old.`
// message -> Hello, my name is Toon and I'm 24 years old.
```

## When to use either?

- Use string formatting when you need to control the format of values in 
  your output.
- Use string interpolation when you want to embed variables directly into a 
  string.
