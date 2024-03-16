# Installing Rust
---
- More details in the following note [[Rust Setup]].

# Create new project:
---
- In your _terminal_ run these commands:
```sh
cargo new your_bevy_prj_name
cd your_bevy_prj_name
```

- After running above commmands, your project folder will have a _tree structure_ like this:
```
│   Cargo.lock
│   Cargo.toml
├───src
|      main.rs
└───target
```

- `main.rs` is your [[Root Crate]] which is the entry point of the program:
```rust
fn main() {
    println!("Hello, world!");
}
```

- `Cargo.toml` is the _"project file"_ which includes:
	- Metadata
	- Dependencies
	- Build configs
```toml
[package]
name = "your_bevy_prj_name"
version = "0.1.0"
edition = "2021"

[dependencies]
```

# Add Bevy to the project:
---

- Method 1: `cargo add bevy`.
- Method 2: Add the following line `bevy = "*"` to your _toml file_:
```toml
[package]
name = "your_bevy_prj_name"
version = "0.1.0"
edition = "2021"

[dependencies]
bevy = "*"
```

- `*` means it will get _the latest version_ of bevy crate. If you want to pick a specific version go to this website and check the version [Bevy](https://crates.io/crates/bevy).

# Compiling optimization:
---
- In case you want to debug the game, the complication is **_super slow_** for doing that. To optimize it, add these following lines in your _toml file_:
```toml
# Enable a small amount of optimization in debug mode
[profile.dev]
opt-level = 1

# Enable high optimizations for dependencies (incl. Bevy), but not for our code:
[profile.dev.package."*"]
opt-level = 3
```

## Optional:
----
### Feature:
- Enable bevy's _dynamic linking [[Feature]]_: 
	- Run `cargo run --features bevy/dynamic_linking` each time.
	- If you don't want to do it each run then add the following feature to your _toml file_:
```toml
[dependencies]
bevy = { version = "0.13.0", features = ["dynamic_linking"] }
```

### Compiler:
- _Nightly Rust Compiler_: Not stable but this gives lightly performance than the _stable rust_.
	- Create _"rust-toolchain.toml"_ file
	- Then put following code:
```toml
[toolchain]
channel = "nightly"
```

### Linker:
- Choose one of following linkers:
- Use _LLD linker_: 
	- Windows: 
```sh
cargo install -f cargo-binutils
rustup component add llvm-tools-preview
```

- Use _mold linker_: x5 faster than _LLD linker_ but not stable and not Windows support
	- **Ubuntu**: `sudo apt-get install mold clang`

### Enable fast compiles:
- Install both LLD linker and nightly rust compiler.
- Put `.cargo/confi`
- Copy following code in the url to `config.toml` file: [link](https://github.com/bevyengine/bevy/blob/main/.cargo/config_fast_builds.toml)

### Rebuild:
- Build your project again to see the significant change.
- The first time may be slow but after that it will be fast.