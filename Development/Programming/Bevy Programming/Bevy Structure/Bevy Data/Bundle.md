Bundle is something similar to class in OOP for our [[Entity]]. It helps you create easily an entity with set of [[Component]]s.

# Bundle as a struct
---
- To create a bundle, pass the trait `Bundle` before your struct:
```rust
#[derive(Component)]
struct PlayerBundle {
	health: f32,
	sprite: SpriteSheetBundle,
	marker: Player,
}
```

- Then, you can spawn the bundle in setup system:
```rust
fn setup(
	mut commands: Commands
) {
	commands.spawn(PlayerBundle {
		health: ...,
		sprite: ...,
		marker: Player,
	});
}
```

- If you want to create an entity with default value, u can derive the **Default** trait for it:
```rust
impl Default for PlayerBundle {
	fn default() -> Self {
		Self {
			health: ...,
			sprite: ...,
			marker: Player,
		}
	}
}
```

- You can then spawn **Player** like this:
```rust
commands.spawn(PlayerBundle {
	health: ...,
	..Default::default()
})
```

# Common mistake
---
- U might think that you can query components by using bundle. But that is wrong. You should always do `Query<(&Component1, &Component2, ...), With<Marker>)` instead.