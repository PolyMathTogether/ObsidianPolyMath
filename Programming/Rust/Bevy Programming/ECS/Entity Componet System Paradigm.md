# Definition:
---
- _ECS_ for shorten is a paradigm that breaks your program into _core components_:
	- [[Enitiy]]: an unique _ID_.
	- [[Component]]: it is the _data field_ of the entity.
	- [[System]]: the _logic_ of the game.

- For example: There is entity _Player_ has two components _HP_ and _Level_. If the player gets enough experience the player will level up. That is called _level_up_ system for _Player_. Or when the enemy hit the _Player_, the _HP_ will be decreased. That is also a system.

# Bevy ECS:
---
- [[Component]]: Rust [[Struct]] with `Component` [[Trait]]
```rust
#[derive(Component)]
struct Position {
	x: i32,
	y: i32,
}
```
- Here we define the type of component `Position`.

- [[System]]: Rust [[Function]]
```rust
fn print_position_system(query: Query<&Position>)
{
	for position in &query {
		println!("x = {}, y = {}", position.x, position.y);
	}
}
```
- [[Query]]

- [[Enitiy]]: A type contains an unique number.
```rust
struct Entity(u64);
```

# Practice
---
## Example 1: Hello World and add system to your app
---
- We will make an app to print "Hello, World!!".
- First we create the _system_ `hello_world`:
```rust
fn hello_world() {
	println!("Hello, World!!");
}
```

- Then add the system to `App`:
```rust
fn main()
{
	App::new()
		.add_systems(Update, hello_world)
		.run()
}
```
- [[Update]]: the [[Schedule]] contains the systems that _run once for per render frame_.
- `add_systems`: this adds the system to the _Update schedule_.

## Example 2: First component
---

- Create a [[Component Marker]] called _Person_:
```rust
#[derive(Component)]
struct Person;
```
- This is Rust's [[Unit Struct]]. For mainly purpose of _marker_. 


- Next, give the _Person_ a component _Name_:
```rust
#[derive(Component)]
struct Name(String);
```

- To add our _Person_ to the [[World]] we use a system called [[Startup]] system.
- Startup: The [[Schedule]] that contains system that:
	- Runs _only once_.
	- Runs before _all other systems_ right after the app _starts_.
```rust
fn add_people(mut commands: Commands) {
	command.spawn((Person, Name("Nguyen Nhat Minh".to_string())));
	command.spawn((Person, Name("Nguyen Hoang Trung".to_string())));
}
```
- This _systems_ will add the _persons_ named "Nguyen Nhat Minh" and "Nguyen Hoang Trung" to our [[World]].
- [[Command]]

- Finally, add the system to the schedule [[Startup]] in our main function:
```rust
fn main()
{
	App::new()
		.add_systems(Startup, add_people)
		.run();
}
```

- To display the data in the [[World]] we create a system to query it:
```rust
fn show(query: Query<&Name, With(Person)>) {
	for name in &query {
		println!("name = {}", name.0);
	}
}
```
- [[With & Without]]

- Then finally add to the [[Update]] schedule:
```rust
fn main()
{
	App::new()
		.add_systems(Startup, add_people)
		.add_systems(Update, show)
		.run();
}
```

- If we want to change the _Name_ of a _Person_, use mut [[Query]]:
```rust
fn change_name(mut query: Query<&mut Name, With<Person>>) {
    for mut name in &mut query {
        if name.0 == "Minh" {
            name.0 = "MINH".to_string();
        }
    }
}
```

- Then add to our main like following code:
```rust
fn main()
{
    App::new()
        .add_systems(Startup, add_people)
        .add_systems(Update, (show, change_name, show).chain())
        .run();
}
```
- `chain()` will order the actions. First show the name then change the name then show it again.