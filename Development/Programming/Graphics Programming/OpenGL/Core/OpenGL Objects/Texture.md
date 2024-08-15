Programmers and artists normally prefer abit **realistic** on their objects. If we have create many **vertices** which have a specific color, it will cost alot performance. That is when **texture** comes in, it basically maps every point data of texture that contain a color to the **surface** via a so-called **texture coordinates**. 

## What is texture?
---
In **computer graphics**, **texture** is the meta-data which describe **the look** of **surface** or **model**. **Image texture** is a **common texture type** that is applied to a **surface** so it will look like the image is "painted" on the **surface**.

![[texture.png]]

In **OpenGL**, an **image** is an **array of pixels** associated with a specific size and format. **OpenGL Texture** is an **OpenGL object** that stores those kinds of image that have the same format. 
## Texture Coordinates
---
If we want to apply a texture to a surface, each point of texture and surface has to be corresponed to eachother.  To define how this mapping is calculated, it needs **texture coordinates**. **Texture coordinates** range from $(0,0)$ to $(1,1)$. In **OpenGL**, $(0, 0)$ is the **bottom left corner**. It uses coordinate axis $(s, t)$ with **2D texture/image texture** and $(s, t, r)$ with **3D texture** (equivalent to $(x,y,z)$).

![[texture_coordinates.png]]

As you can see, the **surface** or the **triangle** on the above image is what we want to paint and the earth image is a **texture**. When using this mapping, the triangle will have a look like a part of the earth. It sounds simple but we're still not quite there yet. When applying the texture to surface, the texture can be shrunk or stretched because the **pixels** in the **texture** not match up one-to-one with **pixels** on **surface**. That is why we need **texture filtering**.

## Texture Filtering
---


