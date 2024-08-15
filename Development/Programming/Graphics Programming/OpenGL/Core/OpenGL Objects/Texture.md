Programmers and artists normally prefer abit **realistic** on their objects. If we have to create many **vertices** which have a specific color, it will cost alot performance. That is when **texture** comes in, it basically maps every point data of texture that contain a color to the **surface** via a so-called **texture coordinates**. 

## What is texture?
---
In **computer graphics**, **texture** is the meta-data which describe **the look** of **surface** or **model**. **Image texture** is a **common texture type** that is applied to a **surface** so it will look like the image is "painted" on the **surface**.

![[texture.png]]

In **OpenGL**, an **image** is an **array of pixels** associated with a specific size and format. **OpenGL Texture** is an **OpenGL object** that stores those kinds of image that have the same format. 
## Texture Coordinates
---
If we want to apply a texture to a surface, each point of texture and surface has to be corresponed to eachother.  To define how this mapping is calculated, it needs **texture coordinates**. **Texture coordinates** range from $(0,0)$ to $(1,1)$. In **OpenGL**, $(0, 0)$ is the **bottom left corner**. It uses coordinate axis $(s, t)$ with **2D texture/image texture** and $(s, t, r)$ with **3D texture** (equivalent to $(x,y,z)$).

![[texture_coordinates.png]]

As you can see, the **surface** or the **triangle** on the above image is what we want to paint and the earth image is a **texture**. When using this mapping, the triangle will have a look like a part of the earth. It sounds simple but we're still not quite there yet. When applying the texture to surface, the texture can be shrunk or stretched because the **pixels** in the **texture** not match up one-to-one with **pixels** on **surface**. That is why we need **texture filtering**. If one **texel** (texture pixel) covers **one or more pixels** in **surface**, texture has to **magnificated** by using **magnification filter**. Otherwise, it needs **minification filter**. 

## Texture Filtering
---
Initially, **pixel** = **texel** and there are two cases:
- **Texture** $\leq$ **surface** (total of texels $\leq$ total of pixels). Texture has to be **magnificated**. After that, **texure** = **surface** and **texel** $\geq$ **pixel**. (**magnification filter**)
![[magnification.png]]
- **Texture** > **surface** (total of texels $>$ total of pixels). Texture has to be **minification**. After that, **texture** = **surface** and **texel** $<$ **pixel**. (**minification filter**)
![[minification.png]]

There are **two basic filtering**, one is **nearest filtering** which chooses color of **nearest textel** to the point of **pixel on surface**. This is fast but it will not give good result. The second one is **linear filtering** which chooses color by taking **average** of **texels** but this is not **inefficient** in case of applying **large texture** to **small surface**.
## Mipmap
---
In case **texture** is larger than **surface**, **linear filtering** will cost alot performance.  So we have to use a solution is called **mipmap** to generate **available copies** of **texture** that are smaller than **orginal** by power of 2.

![[mimapping.png]]

In generally, it will help us find a copy of texture that has the size (total of texels) is equivalent to the size of surface (total of pixels). It costs only about **one-third** more than the memory that original is used but it can do **linear filtering** faster.
$$
\begin{aligned}
&M_{0} \\
&M_{1} = \frac{M_{0}}{4} \\
&M_{2} = \frac{M_{1}}{4} = \frac{M_{0}}{4^2} \\
&\dots \\

&\sum M_{i} = M_{0} \left( 1 + \frac{1}{4} + \frac{1}{4^2} + \dots \frac{1}{4^n} \right) \leq M_{0} + \frac{M_{0}}{3}
\end{aligned}
$$
![[mipmapping2.png]]
