# Definition
---
- It is a **type of data** that has only **one single instance**. Such as configuration / settings. 
- **Resource** is independent with [[Entity]].

# Resource declaration
---
- To create a **resource** type, use trait `Resource` for the [[Struct]]:
```rust
#[derive(Resource)]
struct WindowSettings {
	title: String,
	resolution: (f64, f64),
}
```

- Next we have two ways to add resource to our app:

- With [[Command]]:
```rust
fn setup (
	mut commands: Commands
) {
	commands.insert_resource(WindowSettings { title: "Bevy".into(), resoultion: (500., 300.)});
}
```

- By app builder:
```rust
fn main()
{
	App::new()
		.insert_resource(WindowSettings { title: "Bevy".into(), resoultion: (500., 300.)})
		.run();
}
```

# Resource accessing
---
```rust
fn system(
	my_resource: Res<MyResource>,
	my_mut_resource: ResMut<MyMutResource>,
)
```