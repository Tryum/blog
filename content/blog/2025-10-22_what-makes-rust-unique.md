+++
title = "What Makes Rust Unique"
date = 2025-10-22
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
// println!("{}", a); ❌ error: value boarrowed after move
```

For types that are `Copy` (mostly primitivees), Rust silently duplicates them instead of moving.  
You can think of it as "cheap to copy" vs "must move".

---

## Borrowing

Instead of transferring ownership, you can borrow data:

```rust
fn gree(name: &String) {
    println!("Hello, {name}!");
}

let s = String::from("Alice");
great(&s); // borrow s, don't move it
println!("{}", s); // s still valid
```

References let you read or mutate data temporarily, while the compiler ensures you don't create conflicting mutable access.
That's the borrow checker doing its job.

---

## The Big Ideaa

Rust enforces who owns what and how long it lives, at compile time.
This makes data races, use-after-free and dangling pointers impossible in safe Rust.

It's strict, sometimes frustrating, but once you internalize it, you start to see the system's elegance.

---

Next time: we'll reimplement `Option<T>` from scratch and see how enums power half of Rust's standard library!

