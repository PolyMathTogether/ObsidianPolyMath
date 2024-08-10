It means a **structure** composed by **data** and **state**. For example, [[VBO]] is an **OpenGL object** that helps you manage the GPU memory to store your vertex data and use it as input of [[_Shaders]].

## Common characteristic:
---
- Always has an unique ID.
- Syntax forms:
	- **Generate**: `glGen` - creates reference to the object
	- **Bind**: `glBind` - allocates memory to the object (array, texture or whatever)
	- **Delete**: `glDelete`
- Object Types:
	- **Regular**: contains normal data
		- Buffer
		- RenderBuffer
		- Texture
		- Query
		- Sample
	- **Container**: contains **OpenGL objects** such as [[VAO]]
		- Framebuffer
		- Vertex Array
		- Transform Feedback
		- Program Pipeline