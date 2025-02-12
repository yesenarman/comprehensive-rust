# `Rc`

[`Rc`][1] is a reference-counted shared pointer. Use this when you need to refer
to the same data from multiple places:

```rust,editable
use std::rc::Rc;

fn main() {
    let mut a = Rc::new(10);
    let mut b = a.clone();

    println!("a: {a}");
    println!("b: {b}");
}
```

If you need to mutate the data inside an `Rc`, you will need to wrap the data in
a type such as [`Cell` or `RefCell`][2]. See [`Arc`][3] if you are in a multi-threaded
context.

[1]: https://doc.rust-lang.org/std/rc/struct.Rc.html
[2]: https://doc.rust-lang.org/std/cell/index.html
[3]: ../concurrency/shared_state/arc.md
