> [!info] **WindowPlugin** is one of bevy [[Feature]]s that defines an interface for windowing support.

```rust
use bevy::prelude::{
	*,
	window::WindowTheme
};

WindowPlugin {
	primary_window: Some(
		Window {
			title: "This is title".into(),
			name: Some("bevy.app".into()),
			window_theme: Some(WindowTheme::Dark),
			..Default::default()
		}
	),
	..Default::default()
}
```

- Enable `bevy_winit` to mange window.