# Rc type for single-thread sharing

In Rust, `Rc` (Reference Counted) is a smart pointer that provides shared ownership of a value. `Rc` tracks the number of references to a value. If a new reference is created, `Rc` increments the reference count. If an existing reference is dropped, `Rc` decrements the reference count. When the reference count reaches zero, `Rc` drops the value.

Unlike `Arc` smart pointer, `Rc` cannot be safely shared between threads and is used for single-threaded scenarios.

For example, consider the following code:

```rust
use std::rc::Rc;

fn main() {
    let shared_data = Rc::new(vec![1, 2, 3]);
    let data1 = shared_data.clone();
    let data2 = shared_data.clone();

    println!("{:?}", shared_data);
    println!("{:?}", data1);
    println!("{:?}", data2);
}
```

Here, an `Rc` shares ownership of a vector between multiple references. The `Rc::new()` function creates a new `Rc` that points to a vector of [1, 2, 3]. The `clone()` method creates two new `Rc`s that point to the same vector, and the reference count is incremented. The `println!()` macro prints the values of each reference to the console.

`Rc` is a useful tool for scenarios where shared ownership of a value is needed in a single-threaded environment. By using reference counting to manage the lifetime of the value, `Rc` ensures that the value is not dropped until all references to it have been dropped.
