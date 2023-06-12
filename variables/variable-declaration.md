# Variable Declaration

In Rust, variables are used to store and manipulate data. When declaring variables, you need to specify their type, and by default, variables in Rust are immutable. This means that once a value is assigned to a variable, it cannot be changed.

## Variable Declaration Syntax

To declare a variable, use the `let` keyword followed by the variable name and the type annotation. Here's an example:

```rust
let x: i32 = 42;
```
In the above example, we declare a variable named x of type i32 and assign it the value 42.

### Mutable Variables
To create a mutable variable that can be changed after assignment, use the mut keyword. Here's an example:

```rust
let mut y: f64 = 3.14;
y = 2.71828;
```
In the above example, the variable y is declared as mutable using the mut keyword. We assign an initial value of 3.14 and later update it to 2.71828.

### Type Inference
Rust has a strong type inference system, which means that in many cases, the compiler can automatically infer the type of a variable based on its assigned value. In such cases, you can omit the type annotation. Here's an example:
```rust
let z = "Hello, Rust!";
```
In the above example, the type of the variable z is inferred as &str (string slice) because the assigned value is a string literal.

### Shadowing
Rust allows you to shadow a variable by using the same variable name within a more inner scope. Shadowing allows you to declare a new variable with the same name as an existing one, effectively hiding the previous value. Here's an example:
```rust
let message = "Hello";
let message = message.to_uppercase();
println!("{}", message); // Prints "HELLO"
```
In the above example, we declare a variable named message and then shadow it by declaring a new variable with the same name within a more inner scope. The value of message is changed to its uppercase version using the to_uppercase() method.

### Constants
In addition to variables, Rust also allows you to declare constants. Constants are values that are immutable and must be assigned a value at the time of declaration. Here's an example:
```rust
const PI: f64 = 3.14159;
```
In the above example, we declare a constant named PI of type f64 and assign it the value 3.14159.

### Conclusion
Variables are essential for storing and manipulating data in Rust. Understanding variable declaration, mutability, type inference, shadowing, and constants is crucial for writing effective Rust code.
