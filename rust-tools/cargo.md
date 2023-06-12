# Cargo

Cargo is the package manager and build tool for Rust. It simplifies the process of managing dependencies, building projects, and running tests. Cargo is bundled with the Rust installation.

## Creating a New Rust Project

To create a new Rust project using Cargo, navigate to the desired directory in your terminal and run the following command:

```bash
$ cargo new my_project
This command creates a new directory named my_project containing the basic structure for a Rust project. It also initializes a new Git repository in the project directory by default.

Building and Running a Project
To build a Rust project using Cargo, navigate to the project directory and run the following command:

bash
Copy code
$ cargo build
Cargo will fetch and build any necessary dependencies and compile your project. The resulting executable will be placed in the target/debug directory.

To run the project, use the cargo run command:

bash
Copy code
$ cargo run
Cargo will build the project if necessary and execute the resulting binary.

Dependency Management
Cargo simplifies dependency management by utilizing the Cargo.toml file. This file specifies the project's dependencies and their versions. To add a dependency, open the Cargo.toml file and add the desired crate under the [dependencies] section. For example:

toml
Copy code
[dependencies]
rand = "0.8.4"
After modifying the Cargo.toml file, run cargo build to fetch and compile the dependencies.

Testing
Cargo provides built-in support for writing and running tests. By default, tests are placed in the tests directory. To run the tests for a project, use the cargo test command.

For more advanced usage and detailed information about Cargo, refer to the official Rust documentation: https://doc.rust-lang.org/cargo/
