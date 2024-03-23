### Euclidean Space
The geometry we all are familiar with is the Euclidean Space. There's no curvature in this space-- it is simple to be understood. This is the space we can see in most 3D games, or in a 3D modeling software.
Given a point $P$ in a Euclidean space at the coordinate $(x,y,z)$ and another point $P'$ at $(x+dx, y+dy, z+dz)$, the distance between the two points, $dS$ is easily found from the Pythagorean theorem:
$$
{dS}^2 = {dx}^2 + {dy}^2 + {dz}^2
$$

![[Fig 03.01 Euclidean Distance|25%|center]]

In the case of Euclidean spaces with N dimensions, we can generalize the equation to:
$$
{dS}^2 = \sum_{i=1}^N{dx_i}^2
$$
### Minkowski Space
In special relativity, we studied the Minkowski Space: a 4-Dimensional space with 3 spatial axes and 1 temporal axis. We learnt of the proper time $\tau$, which is in essence, the distance between two points in Minkowski space. It can be found from the frame of reference in which the object of interest is stationary.
$$
c^2{d\tau}^2 = c^2{dt}^2 - {dx}^2 - {dy}^2 - {dz}^2
$$
So we shall define the distance, $dS$, to be
$$
{dS}^2 = {dx}^2 + {dy}^2 + {dz}^2 - c^2{dt}^2
$$
### Other Spaces
A spherical surface is a 2D non-Euclidean space. The distance between two points in differential form is given by:
$$
{dS}^2 = {(R\sin(\theta)d\phi)}^2 + {(Rd\theta)}^2
$$

![[Fig 03.02 Spherical Surface|50%|center]]

![[Fig 03.03 Spherical Right Triangle|25%|center]]
Whereas the distance along a cylindrical surface is
$$
{dS}^2={(Rd\theta)}^2 + {(dz)^2}
$$

![[Fig 03.04 Cylindrical Surface|25%|center]]
![[Fig 03.05 Cylindrical Right Triangle|25%|center]]
There is a way we can generalize this "distance-finding formula". What we are looking for is known as [Differential Geometry](Differential Geometry Pt.1)


