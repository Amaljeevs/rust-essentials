# Heap Memory Management in Rust

In Rust, heap memory is used for dynamically allocating and managing memory. Heap memory provides flexibility in storing data with a variable size and longer lifetimes than stack memory. In this guide, we'll explore how to allocate, deallocate, and manipulate heap memory in Rust.

## Heap Allocation

To allocate memory on the heap in Rust, you can use the `Box<T>` type or other smart pointers. The `Box` type is the simplest way to allocate memory on the heap.

Here's an example of heap allocation using `Box`:

```rust
fn main() {
    let my_number = Box::new(42); // Allocate memory on the heap

    println!("My number is: {}", *my_number); // Access the value using dereference operator *

    // Memory is automatically deallocated when `my_number` goes out of scope
}
```
In this example, we use the Box::new function to allocate memory on the heap and store the value 42. The *my_number syntax is used to dereference the Box and access the value stored on the heap.

### Heap Deallocation
Heap memory in Rust is deallocated automatically when the variable that owns the memory goes out of scope. This automatic deallocation is managed by Rust's ownership system.

However, in some cases, you may need to manually deallocate heap memory. Rust provides the drop trait for customizing the deallocation behavior when an object goes out of scope. Additionally, you can use other smart pointers like Rc or Arc for shared ownership and automatic deallocation when the last reference is dropped.

Here's an example of manually deallocating heap memory using the drop trait:

```rust
struct CustomObject {
    // Fields of the custom object
}

impl Drop for CustomObject {
    fn drop(&mut self) {
        // Custom deallocation logic goes here
        println!("CustomObject is being deallocated");
    }
}

fn main() {
    let obj = CustomObject { /* Initialize fields */ };

    // CustomObject will be deallocated when it goes out of scope
}
```
In this example, the CustomObject struct implements the Drop trait, which allows us to define custom deallocation logic in the drop method. When the obj variable goes out of scope, the drop method is automatically called to deallocate the memory associated with the CustomObject.

### Heap Memory Manipulation
Heap memory in Rust can be manipulated by using functions and methods provided by the standard library. You can allocate dynamic arrays, resize existing allocations, and interact with heap-allocated data using various operations.

Here are a few examples of heap memory manipulation:

```rust
fn main() {
    // Allocate a dynamic array on the heap
    let mut numbers = Vec::new();
    numbers.push(1);
    numbers.push(2);
    numbers.push(3);

    // Resize the array
    numbers.resize(5, 0);

    // Access elements in the array
    let first = numbers[0];
    let last = numbers[numbers.len() - 1];

    println!("First element: {}", first);
    println!("Last element: {}", last);

    // Other operations on heap-allocated data
    // ...
}
```
In this example, we use the Vec type, which represents a dynamic array, to allocate memory on the heap and manipulate the data. We push elements into the array, resize it, and access specific elements using indexing.

### Conclusion
Understanding heap memory management in Rust is essential for handling dynamically allocated data and optimizing memory usage.
