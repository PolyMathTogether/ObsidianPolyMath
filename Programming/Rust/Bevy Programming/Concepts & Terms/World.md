---
up: 
same: ""
down: ""
next: ""
prev: ""
---

# Definition
---
> [!info] 
> - **World** is **data structure** that stores and manages all of the data.
> - You can have **multiple worlds**. 


# Classification of data
---
- There are two kinds of data in Bevy's **World**:
	- [[Entity]]/[[Component]],
	- [[Resource]],

## Entity/Component
---
- You can consisder [[Component]] as column and [[Entity]] as a row in a database.
- [[Entity]] is the `id` field of that table.
- Empty component is called [[Component Marker]].
- Entity/Component can represent as any data you want. It can be even configuration parameters.
- Access: [[Query]].

## Resource
---
- If a data is [[Singleton]] (only one instance) and [[Standalone]] (independent from others) then it is **Resource**. For example: game's graphics settings.
- Access: **Res**.

# Full direct access to the World
---
```rust
fn save_game( 
	// get full access to the World, so we can access all data and do anything world:
	&mut World, 
) { 
	// ... save game data to disk, or something ... 
}
```
- This [[System]] is also known as [[Exclusive Systems]].