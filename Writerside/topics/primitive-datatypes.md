# Primitive Data Types in Go

<deflist> 
    <def title="Go is Strongly and Statically Typed.">
        <p>
            Go, like many strongly-typed languages, includes various 
            primitive data types to represent basic values.
        </p>
        <p>
            These data types are integral to any Go program's 
            functionality.
        </p>
    </def>
</deflist>

```Go
bool

string

int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr

byte // alias for uint8

rune // alias for int32
     // represents a Unicode code point

float32 float64

complex64 complex128

nil

const
```

1. `bool`: 
    - Represents a Boolean value, which can be either `true` or 
      `false`. 
    - Used for logical comparisons and control flow.

2. `string`:
    - Represents a sequence of characters. 
    - Strings are immutable, meaning they cannot be modified once created.

3. `int` and `uint`:
   1. `int`: 
      - Represents signed integers. 
      - Its size depends on the underlying architecture (32 or 64 bits).
   2. `uint`:
      - Represents unsigned integers, meaning it cannot hold negative 
        values.

   {style="alpha-lower"}

{collapsible="true" default-state="collapsed"}
Other int and uint
: - Go provides various integer data types with different sizes and ranges
to suit different needs.
- Specifically, the integer types in Go include int8, int16, int32, int64, 
  uint8, uint16, uint32, and uint64. The numbers in their names indicate the 
  size of memory used to store the variable (8, 16, 32, 64, etc.),
  representing the number of bits.

> When would I deviate from using default types? <br/> <br/>
> You may choose custom types when built-in types lack the needed behavior, 
> constraints, or additional features.
> 
 {style="note"}

4. `float32` and `float64`:
    1. `float32`:
        - Represents single-precision floating-point numbers, which are 
          suitable for most floating-point calculations.
    2. `float64`:
        - Represents double-precision floating-point numbers, offering 
          higher precision but using more memory.

   {style="alpha-lower"}

5. `byte` and `rune`:
    1. `byte`:
        - An alias for `uint8`, or 8 bits.
        - Used to represent individual bytes or small integer values.
        - Use cases including marshalling a json object to be sent across a 
          network connection or reading to and from a file on the disk.
    2. `rune`:
        - An alias for `int32`. 
        - Used to represent Unicode code points, generally speaking a 
          character in a string.
        - Useful for working with international characters.

   {style="alpha-lower"}

6. `complex64` and `complex128`:
    1. `complex64`:
        - Represents complex numbers with float32 real and imaginary parts.
    2. `complex128`:
        - Represents complex numbers with float64 real and imaginary parts.

   {style="alpha-lower"}

7. `uintptr`:
    - Represents an unsigned integer large enough to store the 
      uninterpreted bits of a pointer value. 
    - Used primarily in low-level programming.

8. `nil`:
    - Represents the absence of a value. 
    - It's a zero value for pointers, functions, interfaces, slices, 
      channels, and maps.

9. `const`:
    - A type representing constants in Go. 
    - Constants are values with a fixed and unchanging value.

These primitive data types form the building blocks for more complex 
data structures and custom data types in Go.