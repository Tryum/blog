+++
title = "The journey begins"
date = 2025-10-24
description = "A candid reflection on interviewing, gaps in Rust fundamentals, and a plan to relearn Rust through byte-sized posts."
tags = ["rust", "learning", "copy-on-write", "career", "reading-plan"]
+++

TL;DR: I realized gaps in my Rust fundamentals after a tough interview (hello `Cow`). I’m going back to basics: reading the Rust books end-to-end and writing short posts about core concepts.

## Why I’m writing this

At the end of October 2025, my previous company, Metagravity, shut down. As I started looking for a new role, the rejections piled up.
Some were fair, I’m missing a few in-demand skills (Kubernetes is hot right now). Others cut deeper: my Rust knowledge wasn’t as solid as I thought. One interview made that painfully clear. A question about Rust’s Cow ([copy-on-write][cow]) put me on the spot. I knew the concept, but I hadn’t used it in Rust, and I struggled with the problem. Stress took over, and I even stumbled on basics. That shook my confidence. After a few days of reflection, I took it as a wake-up call: I’ve had a strong career as a software engineer, but my Rust fundamentals need work.

When I first learned C, I read [**The C Programming Language**][1] by Kernighan and Ritchie. When I learned C++, I read [**C++ How to Program**][2] by Deitel and Deitel. After 17 years as a software engineer, I started to work professionally with Rust in 2023. I started to read [**The Rust Programming Language**][3] and  [**the Brown University edition**][4], but I skimmed them, and started to code right away. I learned numerous things on the job, but I never really took the time to solidify my knowledge.

## What I’ll do next

So I decided to go back to basics. I will read Rust books from cover to cover, and write blog posts about what I learn. This will help me solidify my knowledge, and also share what I learn with others. I'll aim to write small, "byte-sized" posts that can be read in less than 10 minutes, explaining a core concept, or a specific feature of Rust or its standard library.

This is the first post in this journey. I hope you will find it useful.  
If you’re learning Rust too, subscribe or leave a comment with topics you’d like me to cover.

[cow]: https://doc.rust-lang.org/std/borrow/enum.Cow.html
[1]: https://www.cprogramming.com/books/ritchie.html
[2]: https://deitel.com/c-plus-plus-how-to-program-10-e/
[3]: https://doc.rust-lang.org/stable/book/
[4]: https://rust-book.cs.brown.edu/
