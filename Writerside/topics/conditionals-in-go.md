# Conditionals In Go

## The if else statement
The `if` statement is a fundamental construct in the Go programming language 
that allows you to make decisions and control the flow of your program based 
on certain conditions. <br/> It is used to execute a block of code if a 
specified condition is `true`.

```Go
if score >= 80 {
    fmt.Println("A grade")
} else if score >= 60 {
    fmt.Println("B grade")
} else {
    fmt.Println("C grade")
}
```

### Initial Statement of an IF Block
In Go, you can include an initial statement before the condition in an if 
statement. This is particularly useful when you want to initialize a 
variable and limit its scope within that if block.

```Go
if length := getHeight(person); length < 110 {
    fmt.Println("Too dangerous for this rollercoaster.")
}
```

## Select Statement

The `select` statement in Go is a powerful construct used for handling 
concurrent operations and communication through `channels`. It's often
used in `Goroutines` for concurrency. <br/> <br/>
The `select` statement is used with `channels` to perform non-blocking
communication. It allows you to choose the first `channel` operation that can
proceed, making it useful for handling concurrent code.

```Go
select {
case result := <-dataChannel:
    fmt.Println("Received data:", result)
case <-time.After(5 * time.Second):
    fmt.Println("Timeout: No data received.")
}

// In this example, the program waits for data on dataChannel but will time 
// out if no data arrives within 5 seconds.
```

### Key Takeaways from Select Statement

1. **Blocking Behavior:**
   - The `select` statement blocks until one of the `channel` operations is 
     ready to proceed. 
   - If none are ready, it will block or execute the code in the `default` 
     case if it's present.

2. **Order of Execution:** 
   - The order of execution is determined by the first case that can proceed. 
   - If multiple cases can proceed at the same time, one will be chosen at 
     random.
3. **Default Case:**
    - The `default` case is **optional** and is executed when no other 
     case can proceed. 
    - It's useful for non-blocking operations or for handling situations 
      when none of the `channel` operations are ready.

### Use cases for Select Statement

1. **Goroutine Coordination:** `select` is commonly used to coordinate multiple 
`Goroutines` by allowing them to communicate through channels.

2. **Timeout Handling:** You can use `select` with a time. After `channel` to 
   implement timeouts for certain operations. 

3. **Non-blocking Operations:** `select` is valuable for handling 
   non-blocking `channel` operations to prevent `Goroutines` from getting stuck. 

4. **Fanning Out and Selecting Fastest Result:** It can be used to fan out
   requests to multiple services and `select` the result from the service that 
   responds the fastest.

## The Switch Statement

The `switch` statement allows you to evaluate an expression and execute 
different code blocks based on the matching `case`.

```Go
switch day {
case "Monday":
    fmt.Println("It's Monday.")
case "Tuesday", "Wednesday":
    fmt.Println("It's a weekday.")
default:
    fmt.Println("It's the weekend.")
}
```