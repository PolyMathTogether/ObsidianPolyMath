---
title: My setup
Linker: LLD
Compiler: Nightly Rust compiler
---
# config.toml:
```toml
# Add the contents of this file to `config.toml` to enable "fast build" configuration. Please read the notes below.

# NOTE: For maximum performance, build using a nightly compiler
# If you are using rust stable, remove the "-Zshare-generics=y" below.

[target.x86_64-unknown-linux-gnu]
linker = "clang"
rustflags = [
  "-Clink-arg=-fuse-ld=lld", # Use LLD Linker
  "-Zshare-generics=y",      # (Nightly) Make the current crate share its generic instantiations
  "-Zthreads=0",             # (Nightly) Use improved multithreading with the recommended amount of threads.
]

# NOTE: you must install [Mach-O LLD Port](https://lld.llvm.org/MachO/index.html) on mac. you can easily do this by installing llvm which includes lld with the "brew" package manager:
# `brew install llvm`
[target.x86_64-apple-darwin]
rustflags = [
  "-Clink-arg=-fuse-ld=/usr/local/opt/llvm/bin/ld64.lld", # Use LLD Linker
  "-Zshare-generics=y",                                   # (Nightly) Make the current crate share its generic instantiations
  "-Zthreads=0",                                          # (Nightly) Use improved multithreading with the recommended amount of threads.
]

[target.aarch64-apple-darwin]
rustflags = [
  "-Clink-arg=-fuse-ld=/opt/homebrew/opt/llvm/bin/ld64.lld", # Use LLD Linker
  "-Zshare-generics=y",                                      # (Nightly) Make the current crate share its generic instantiations
  "-Zthreads=0",                                             # (Nightly) Use improved multithreading with the recommended amount of threads.
]

[target.x86_64-pc-windows-msvc]
linker = "rust-lld.exe" # Use LLD Linker
rustflags = [
  "-Zshare-generics=n", # (Nightly)
  "-Zthreads=0",        # (Nightly) Use improved multithreading with the recommended amount of threads.
]

# Optional: Uncommenting the following improves compile times, but reduces the amount of debug info to 'line number tables only'
# In most cases the gains are negligible, but if you are on macos and have slow compile times you should see significant gains.
#[profile.dev]
#debug = 1
```
# Cargo.toml:
```toml
[package]
name = "bevy_game_test"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]

[dependencies.bevy]
version = "0.13.0"

# Disable all Bevy default features
default-features = false

# Enable Bevy feature
features = [
    # Bevy functionality:
    "bevy_winit",	
    "bevy_asset",
    
    # Bevy formats:
    "png",
    
    # Development/Debug features:
    "dynamic_linking",
]

# Enable a small amount of optimization in debug mode
[profile.dev]
opt-level = 1

# Enable high optimizations for dependencies (incl. Bevy), but not for our code:
[profile.dev.package."*"]
opt-level = 3
```
