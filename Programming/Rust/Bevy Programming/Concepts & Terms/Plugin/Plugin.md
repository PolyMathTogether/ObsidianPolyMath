---
up: 
same: ""
down: ""
next: '"[[]]"'
prev: '"[[Entity Component System Paradigm]]"'
---
# Bevy plugins:
---
- All bevy [[Feature]]s can be consisder as _**plugins**_.
- Plugin is **collection of code** used to modify the _App_.
- You can disable a [[Feature]] if you don't want it in app.
- You can also build your own _plugin_. If it doesnt contribute to Bevy, it is called _3rd-party plugin_. To use other's 3rd-party plugin have to do:
	- Search plugins on [Bevy Assets](https://bevyengine.org/assets/).
	- Add it under the `[dependencies]` in `Cargo.toml` file.
	- Import to `main.rs` by `use third-party::prelude:*;`.
	- Add the plugin to the app `.add_plugins(third-party-plugin)`.
- In case you want to use **Bevy Plugins**. Bevy has a set of plugins called [[DefaultPlugins]].
