# Rhai script

Rhai is an embedded scripting language for Rust. Rhai is a dynamically typed language with support for high-level data types such as arrays, maps, and functions. Rhai supports Rust-style ownership and borrowing, making it easy to integrate with Rust's memory management.

One of the key features of Rhai is its safety and security. Rhai enforces sandboxing by default, which means that scripts executed within a Rhai interpreter cannot access or modify the host environment. Rhai also supports a variety of security features such as timeouts, memory limits, and access controls to ensure that scripts are safe to use.

Rhai's syntax is similar to Rust's syntax, making it easy for Rust developers to learn and use. Rhai also provides a number of built-in functions and operators that simplify common scripting tasks such as string manipulation, math operations, and control flow.

Example of using Rust as an embedded language in Rhai script:

```rust
use rhai::{Engine, EvalAltResult};

fn main() -> Result<(), Box<dyn std::error::Error>> {
    let mut engine = Engine::new();

    let result = engine.eval::<i32>("2 + 2")?;
    println!("2 + 2 = {}", result); // should print 4

    let result = engine.eval::<f64>("3.14 * 2.0")?;
    println!("3.14 * 2.0 = {}", result); // should print 6.28

    let result = engine.eval::<i32>("10 / 3")?;
    println!("10 / 3 = {}", result); // should print 3

    Ok(())
}
```

In this example, the Rhai script evaluates arithmetic expressions, and Rust performs the actual calculations. This combines Rhai's dynamic code and Rust's strong typing and optimized performance.
