# Shadowing in Rust

Shadowing is a feature in Rust that allows you to declare a new variable with the same name as an existing variable, effectively hiding the previous value. It provides flexibility and allows you to reuse variable names without conflict.

## Shadowing Syntax

To shadow a variable, you simply declare a new variable with the same name within a more inner scope. Here's an example:

```rust
let x = 42;

{
    let x = "hello";
    println!("{}", x); // Prints "hello"
}

println!("{}", x); // Prints 42
```
In the above example, we have two variables named x, but they exist in different scopes. The inner x shadows the outer x within the block. Therefore, when we print the value of x within the inner scope, it prints "hello", and when we print it outside the inner scope, it prints 42.

### Shadowing and Data Type Conversion
Shadowing can also be used to change the data type of a variable. By redeclaring the variable with a different data type, you can effectively change its type without the need for explicit type casting. Here's an example:

```rust
let x = "42";
let x = x.parse::<i32>().unwrap();
println!("{}", x); // Prints 42
```
In the above example, we initially declare x as a string. Then, by shadowing x and using the parse method, we convert it to an i32 data type. The final print statement correctly outputs the converted integer value.

### Shadowing and Mutable Variables
Shadowing can also be used with mutable variables. By shadowing a mutable variable, you can change its value while keeping the mutability intact. Here's an example:

```rust
let mut x = 42;
x = 10; // Mutable assignment

let x = x * 2; // Shadowing with new value
println!("{}", x); // Prints 20
```
In the above example, we declare x as a mutable variable and assign an initial value of 42. Then, by shadowing x with a new value, we multiply the original value by 2 and print the result.

### Conclusion
Shadowing in Rust allows you to declare a new variable with the same name as an existing variable, effectively hiding the previous value. It provides flexibility in reusing variable names, changing data types, and modifying mutable variables while maintaining clear scoping boundaries.
