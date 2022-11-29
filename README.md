# libefi-sys

Bindings to the libefi library on illumos.

## Construction

This library is built using bindgen, following this tutorial:
<https://rust-lang.github.io/rust-bindgen/command-line-usage.html>

Specifically, this was generated with:

```bash
$ bindgen --version
bindgen 0.63.0

$ bindgen wrapper.h -o src/lib.rs
```

The bindings are then modified to allow compilation without warning.
This is done by prepending the following to `lib.rs`.

```rust
#![allow(non_upper_case_globals)]
#![allow(non_camel_case_types)]
#![allow(non_snake_case)]
```
