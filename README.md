<div align="center">
  <h1><code>unsafe-io</code></h1>

  <p>
    <strong>Non-owning unsafe I/O</strong>
  </p>

  <p>
    <a href="https://github.com/sunfishcode/unsafe-io/actions?query=workflow%3ACI"><img src="https://github.com/sunfishcode/unsafe-io/workflows/CI/badge.svg" alt="Github Actions CI Status" /></a>
    <a href="https://crates.io/crates/unsafe_io"><img src="https://img.shields.io/crates/v/unsafe_io.svg" alt="crates.io page" /></a>
    <a href="https://docs.rs/unsafe-io"><img src="https://docs.rs/unsafe-io/badge.svg" alt="docs.rs docs" /></a>
  </p>
</div>

This is a very low-level library that just serves to factor out
platform-specific code for working with platform-specific handle types such
as [`RawFd`], [`RawHandle`], and [`RawSocket`].

Being non-owning, these handles operate much like raw pointers in Rust. They
are considered safe to construct, but unsafe to use in any way that depends on
the resource they point to.

[`RawFd`]: https://doc.rust-lang.org/std/os/unix/io/type.RawFd.html
[`RawHandle`]: https://doc.rust-lang.org/std/os/windows/io/type.RawHandle.html
[`RawSocket`]: https://doc.rust-lang.org/std/os/windows/io/type.RawSocket.html
