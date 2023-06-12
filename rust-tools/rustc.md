# Rustc

Rustc is the Rust compiler, responsible for translating Rust source code into executable machine code. It is a command-line tool that comes bundled with the Rust programming language.

## Basic Usage

To compile a Rust source file, you can use the `rustc` command followed by the file name with the `.rs` extension. Here's an example:

```bash
$ rustc hello.rs 
This command will compile the hello.rs file and generate an executable file named hello (or hello.exe on Windows) in the same directory.

Compilation Options
The rustc command provides various options to control the compilation process. Here are some commonly used options:

* '-o <output>': Specifies the name of the output file. For example, rustc hello.rs -o greetings will generate an executable file named greetings.
* '--release': Performs an optimized release build. Use this option to generate optimized code with better performance.
* '--crate-type <type>': Specifies the type of output to produce. The available types are bin (executable), lib (library), and rlib (Rust static library).
For more information about the rustc command and its options, you can refer to the official Rust documentation: https://doc.rust-lang.org/rustc/
