# Function Basics in Rust

Functions are an essential part of any programming language, including Rust. They allow you to encapsulate reusable blocks of code and execute them when needed. In this guide, we'll cover the basics of defining and using functions in Rust.

## Function Syntax

Here's the basic syntax for defining a function in Rust:

```rust
fn function_name(parameter1: Type1, parameter2: Type2) -> ReturnType {
    // Function body
    // Code to be executed
    // Return statement (if applicable)
}
```

> fn: The keyword used to define a function.
function_name: The name of the function.
parameter1, parameter2: The parameters (inputs) of the function, along with their types.
ReturnType: The type of value that the function returns.
->: The arrow operator used to specify the return type.
Function body: The code block enclosed within curly braces {} that represents the function's implementation.

### Function Example
Here's an example of a simple function that calculates the sum of two numbers and returns the result:

```rust
fn sum(a: i32, b: i32) -> i32 {
    let result = a + b;
    result // Implicit return statement
}
```
In this example, the sum function takes two parameters a and b of type i32. It calculates the sum of a and b and assigns the result to a variable named result. Finally, the function implicitly returns the value of result.

### Calling a Function
To execute a function and use its result, you need to call the function. Here's an example of calling the sum function and printing the result:

```rust
fn main() {
    let a = 5;
    let b = 3;

    let result = sum(a, b);
    println!("The sum is: {}", result);
}
```
In this example, we define a main function as the entry point of the program. Inside the main function, we declare two variables a and b and assign them values. Then, we call the sum function with a and b as arguments and store the returned value in the result variable. Finally, we print the result using the println! macro.

### Conclusion
Functions are powerful building blocks in Rust that enable code reuse and modularity. Understanding function syntax, defining parameters and return types, and calling functions is essential for writing Rust programs.
