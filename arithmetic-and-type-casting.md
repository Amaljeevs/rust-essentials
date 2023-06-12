# Arithmetic and Type Casting in Rust

Rust provides a rich set of operators for performing arithmetic operations on numeric types. Additionally, it supports type casting to convert values between different data types.

## Arithmetic Operators

Rust supports the following arithmetic operators:

- `+` (addition)
- `-` (subtraction)
- `*` (multiplication)
- `/` (division)
- `%` (remainder/modulo)
- `+=` (addition assignment)
- `-= ` (subtraction assignment)
- `*=` (multiplication assignment)
- `/=` (division assignment)
- `%=` (remainder/modulo assignment)

Here's an example that demonstrates the usage of these operators:

```rust
fn main() {
    let a = 5;
    let b = 2;

    let sum = a + b;
    let difference = a - b;
    let product = a * b;
    let quotient = a / b;
    let remainder = a % b;

    println!("Sum: {}", sum);
    println!("Difference: {}", difference);
    println!("Product: {}", product);
    println!("Quotient: {}", quotient);
    println!("Remainder: {}", remainder);
}
```
In the above example, we declare two variables a and b, and perform various arithmetic operations to calculate their sum, difference, product, quotient, and remainder.

### Type Casting
Type casting is the process of converting a value from one data type to another. Rust provides the as keyword for performing type casting. Here's an example:

```rust
fn main() {
    let a: i32 = 42;
    let b: f64 = a as f64;
    let c: u8 = b as u8;

    println!("Original: {}", a);
    println!("After casting to f64: {}", b);
    println!("After casting to u8: {}", c);
}
```
In the above example, we initially declare a variable a of type i32. We then perform type casting to convert a to a f64 type using the as keyword. Finally, we cast b to a u8 type.

### Conclusion
Arithmetic operations and type casting are important concepts in Rust. With the available arithmetic operators, you can perform various calculations on numeric types. Type casting allows you to convert values between different data types as needed.
