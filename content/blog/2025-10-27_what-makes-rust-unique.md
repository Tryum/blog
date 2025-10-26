+++
title = "What Makes Rust Unique"
date = 2025-10-27
draft = true
+++

Every language has its perks and unique features, Rust stands out by achieving performance and safety !  
The compiler, friend and foe, enforces ownership and borrowing at compile time, so you get memory safety without a garbage collector.

Let's unpack that in 5 minutes.

---

## Ownership

In Rust, every value has exactly one owner. When that owner goes out of scope, the value is dropped automatically.

```rust
{ 
    let s = String::from("Hello");
    // s is valid here
} // s goes out of scope -> memory is freed
```

No `free()`, no GC. Just automatic cleanup.

---

## Moves and Copies

When you assign or pass values, ownership usually moves, not copies:

```rust
let a = String::from("hi");
let b = a; // a is moved into b
// println!("{}", a); ❌ error[E0382]: borrow of moved value: `a`
```

[Link to Rust Playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2024&gist=326265a029e71e9ea73585fd8f927ca5)

For types that are `Copy` (mostly primitivees), Rust silently duplicates them instead of moving.  
You can think of it as "cheap to copy" vs "must move".

---

## Borrowing

Instead of transferring ownership, you can borrow data:

```rust
fn great(name: &String) {
    println!("Hello, {name}!");
}

fn main() {
    let s = String::from("Alice");
    great(&s); // borrow s, don't move it
    println!("{}", s); // s still valid
}
```

[Link to Rust Playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2024&gist=1dc8a2b6b50fd98525b05893264a8149)

References let you read or mutate data temporarily, while the compiler ensures you don't create conflicting mutable access.
That's the borrow checker doing its job.

---

## The Big Idea

Rust enforces who owns what and how long it lives, at compile time.
This makes data races, use-after-free and dangling pointers impossible in safe Rust.

It's strict, sometimes frustrating, but once you internalize it, you start to see the system's elegance.

---

Next time: we'll reimplement `Option<T>` from scratch and see how enums power half of Rust's standard library!
