# Rust CLI Tools

- [Rust CLI Tools](#rust-cli-tools)
  - [Cargo Audit](#cargo-audit)
  - [Cargo Checkmate](#cargo-checkmate)


## Cargo Audit

[cargo-audit](https://crates.io/crates/cargo-audit) is a crate that provides
security vulnerability context for packages found in the Cargo.lock file.

* Install:
  * `cargo install cargo-audit`
* Configure:
  * `audit.toml`
* Run:
  * `cargo audit`

## Cargo Checkmate

[cargo-checkmate](https://crates.io/crates/cargo-checkmate) is a crate that
runs all of the common utilities for checking your Rust project. This includes:

* `cargo check`
* `cargo format`
* `cargo clippy`
* `cargo build`
* `cargo test`
* `cargo doc`
* `cargo audit`

* Install:
  * `cargo install cargo-checkmate`
* Configure:
  * `cargo checkmate git-hook install` to install the git hook
  * `cargo checkmate github-ci install` to add a GitHub action
* Run:
  * `cargo checkmate`
