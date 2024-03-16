# Bring bevy to the app:
---
- After finishing the [[Bevy Setup]] part. You can start coding by adding `use bevy::predule::*` to the `main.rs` source file:

```rust
use bevy::prelude::*;

fn main()
{
	println!("Hello World");
}
```

- By doing this, it will bring all [[Path]]s to your main program.

# First basic program:
---
- The _first_ and _important component_ you have to have in your program is `App`:
```rust
use bevy::prelude::*;

fn main()
{
	App::new()
		.run();
}
```
- Initializes new `App` by `App::new()` then `.run()` it.
> [!tip] You can consider App as the Bevy Program

What is App:
---
- An [App](https://docs.rs/bevy/latest/bevy/app/struct.App.html): in the docs, there are three fields:
	- [[World]]: stores all game's datas.
	- [[Schedule]]: a collection of [[System]]s.
	- [[Runner]]: bases on schedules, the runner controls the broad execution strategy.

