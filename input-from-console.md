# Input from Console

Rust provides several ways to read input from the console. Depending on your requirements, you can choose the appropriate method for reading user input.

## Using the `std::io` Module

The `std::io` module in Rust provides utilities for reading input from the console. The most common method is to use the `stdin` function from the `std::io` module in combination with the `read_line` method to read input as a string. Here's an example:

```rust
use std::io;

fn main() {
    let mut input = String::new();

    println!("Enter your name: ");
    io::stdin().read_line(&mut input).expect("Failed to read input");

    println!("Hello, {}!", input);
}
```
In the above example, we create a mutable input variable of type String to store the user input. We use the read_line method to read input from the console and store it in the input variable.

### Parsing Input
If you need to read input of a specific type, such as an integer or a floating-point number, you can use Rust's parsing capabilities to convert the input string to the desired type. Here's an example:

```rust
use std::io;

fn main() {
    let mut input = String::new();

    println!("Enter a number: ");
    io::stdin().read_line(&mut input).expect("Failed to read input");

    let number: i32 = input.trim().parse().expect("Invalid number");

    println!("You entered: {}", number);
}
```
In this example, we read a number as input from the console and parse it into an i32 type using the parse method. The trim method is used to remove any leading or trailing whitespace characters before parsing.

### Using External Crates
If you require more advanced input handling, such as parsing complex data structures or handling user prompts, you can explore external crates like dialoguer or readline. These crates provide additional functionality for handling user input with features like prompts, menus, and more.

### Conclusion
Reading input from the console is a common requirement in many programs. By using the std::io module and Rust's parsing capabilities, you can efficiently read and process user input.
