# Memory Comparison: Go vs. Other Languages

## Go Programs Keep It Light

<img src="$PROJECT_DIR$/Writerside/images/garbage-collection.png" 
alt="Garbage Collection Java, Go, and Rust/C" width="600" style="inline"/>

Credits for [Computer fire][computer-burning] png


- 'Go' programs are known for their memory efficiency. 
- Each 'Go' program includes a small, additional component called the 
  'Go Runtime', which is embedded within the executable binary. 
- The 'Go Runtime' plays a crucial role in optimizing memory usage by
  cleaning up unused memory dynamically as the program runs.

## Side-by-Side Comparison

<img src="$PROJECT_DIR$/Writerside/images/idle-memory-usage.png" 
alt="Idle Memory Usage Chart by Dexter Darwich" width="500" style="inline"/>

*[Dexter Darwich's chart][dexter-darwich] displays idle memory usage 
same application in three languages.*

When we compare memory usage, some patterns emerge:

- **Java vs. Go:** 
  - In general, Java programs tend to consume more 
    memory compared to their Go counterparts. 
  - This is because Java relies on a full-fledged virtual machine, 
    whereas Go uses a minimal runtime. 
  - The Go runtime is so compact that it becomes an integral part of each 
    Go programs compiled machine code.

- **Rust and C++ vs. Go:** 
  - Rust and C++ programs, on average, use slightly less memory than Go 
    programs. 
  - This is due to the level of control they offer to developers for 
    optimizing memory usage. In Go, the runtime automatically handles 
    memory management, which simplifies things but may result in 
    slightly higher memory usage.


{style="full"}
Go achieves Balance
: So, when it comes to memory, Go strikes a balance between ease of use 
and efficient memory management. Java is known for its thirst for 
memory, while Rust and C++ provide a bit more control for those who 
want to fine-tune memory consumption.

[dexter-darwich]: https://medium.com/@dexwritescode/comparison-between-java-go-and-rust-fdb21bd5fb7c
[computer-burning]: https://www.rawpixel.com/search/computer%20crashes?page=1&path=_topics&sort=curated