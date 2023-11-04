# Type Casting In Go

Type casting is the process of converting a value of one data type into 
another. In Go, you can perform type casting when necessary to ensure 
compatibility between different data types.

### Casting Between Numeric Types

Casting between numeric types is quite straightforward.

```Go
var x float64 = 42.5
var y int = int(x)  // Casting from float64 to int -> 42
```

> If you cast a floating point integer to an integer, the floating points 
> are truncated.

### Casting from String

```Go
var numStr string = "123"
var num int = 0

// Using strconv.Atoi to cast a string to an integer, and discarding the error
num, _ = strconv.Atoi(numStr)
```

The `strconv.Atoi()` function returns two values. The first value is the result
of the conversion (an integer), and the second value is an error. By using
the underscore, you're indicating that you don't intend to use or handle the
error in this specific case.

### Casting to String 

```Go
var value float64 = 42.0

// Casting from float64 to string
var valueStr string = strconv.FormatFloat(value, 'f', -1, 64)
```

In this example, we have a float64 variable `value` with the value `42.0`. We 
use the `strconv.FormatFloat()` function to cast this floating-point number 
to a string, and the result is stored in the `valueStr` variable. As a result, 
`valueStr` now contains the string representation of the value, which is `"42"`.

```Go
num := 42 
numStr := strconv.Itoa(num)  // Convert int to string
```

In this example, we have an integer `num`, and we use `strconv.Itoa()` to 
convert it to a string. The resulting `numStr` variable now holds the string 
representation of the integer.

### Casting using Type Assertion

```Go
var val interface{} = 42
num, ok := val.(int)  // Type assertion for interface{} to int
if ok {
    // Casting successful
    fmt.Println("Casting successful:", num)
} else {
    // Casting failed
    fmt.Println("Casting failed")
}
```

In this example, we have an `interface{}` variable `val` containing the 
value `42`. We use type assertion to attempt to convert it to an `int`. If the 
casting is successful, it prints "Casting successful" along with the value 
of `num`. If the casting fails, it prints "Casting failed".

### Casting Pointers

```Go
var x int = 42
var ptr *int = &x
var ptrStr string = fmt.Sprintf("%p", ptr)  // Casting a pointer to a string
```

In this example, we have an integer `x` with the value `42`, and we create a 
pointer `ptr` that points to `x`. We use the `fmt.Sprintf()` function to cast 
the pointer to a string, and the resulting `ptrStr` variable now contains 
the string representation of the pointer's memory address.

### Casting to and from Bytes

```Go
str := "Hello, Go!"
bytes := []byte(str)  // Casting from string to bytes
str2 := string(bytes)  // Casting from bytes to string
```

In this example, we start with a string `str` containing `"Hello, Go!"` and use 
`[]byte(str)` to cast it to a byte slice. Then, we use `string(bytes)` to cast 
the byte slice back to a string. As a result, `str2` now contains the same 
string as `str`.


