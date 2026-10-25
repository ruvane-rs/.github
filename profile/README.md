<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ruvane-rs/.github/main/profile/assets/ruvane-hero-dark.svg">
  <img src="https://raw.githubusercontent.com/ruvane-rs/.github/main/profile/assets/ruvane-hero-light.svg" alt="Ruvane — One language. The whole web. An experimental Rust web framework." width="1200" height="400">
</picture>

<p align="center">
  <a href="https://crates.io/crates/ruvane"><img src="https://img.shields.io/crates/v/ruvane?style=flat-square&label=crates.io&color=c36b4b" alt="Published version on crates.io"></a>
  <a href="https://docs.rs/ruvane"><img src="https://img.shields.io/badge/API-docs-686b73?style=flat-square" alt="API documentation"></a>
  <a href="https://github.com/ruvane-rs/.github/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-686b73?style=flat-square" alt="MIT license"></a>
</p>

<p align="center">
  <b>A Rust web stack, built from first principles.</b><br>
  One language from the server to the browser. Zero third-party dependencies.
</p>

We're building **Ruvane**, an experimental web framework that brings server
rendering, browser interactivity, and development tools into one coherent Rust
stack. The framework, reactive runtime, browser adapter, and CLI are all built
in-house, on top of Rust's standard library and native browser APIs.

### One connected stack

The framework in development brings together:

| Server | Browser | Tooling |
| :--- | :--- | :--- |
| Typed HTML, routing, shared layouts, native forms, and static export. | Rust through WebAssembly, reactive state, hydration, and persistent client layouts. | Project scaffolding, local development, and versioned builds with the `ruvane` CLI. |

### Built with intention

- **Own the foundations.** Zero third-party crates or npm packages, including build and test dependencies.
- **Make behavior explicit.** Typed composition, scoped reactive state, and deliberate resource limits.
- **Start with HTML.** Server-rendered pages and native links and forms, enhanced with Rust in the browser.

### Try the published crate

Ruvane is in **early alpha**. The main repository is currently private and APIs
can change. The published **alpha.2** focuses on HTML rendering and local HTTP
serving; the browser runtime and CLI described above are part of ongoing development.

In an existing Rust project:

```sh
cargo add ruvane@=0.1.0-alpha.2
```

```rust
use ruvane::{Document, Tag, element};

fn main() {
    let page = Document::new(
        "Hello, Ruvane",
        element(Tag::H1).child("The web, in Rust."),
    );

    println!("{}", page.render());
}
```

Explore the [published crate](https://crates.io/crates/ruvane) and
[API documentation](https://docs.rs/ruvane/0.1.0-alpha.2/ruvane/).
Requires Rust 1.85 or newer.

---

<p align="center"><sub>Built from scratch in Rust. Released under the MIT license.</sub></p>
