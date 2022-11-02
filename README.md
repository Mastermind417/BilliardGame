# BilliardGame
A two dimensional simulation in `Processing` that represents an actual billiard game/table. 

![](images/initial_position.png)

The program can be interacted by one or two players as to play a virtual pool game. 

The project focuses on the implementation of two dimensional physics in a game. Artistic emphasis was not the primary goal of this implementation. Visual effects were implemented to a minimal standard as to represent a 2D billiard table to a satisfactory level. Visual aesthetics such as lighting and white ball lining may be implemented in the future, if time permits.

The final product is inspired by a usual 2D billiard table found on the Web.

![](images/pool.jpg)

## Visualisation

The billiard layout is broken into fundamental billiard "pieces". These are shown in the picture below:

![](images/layout_explanation_img.jpg)

Each billiard piece is represented by primitive shapes in `Processing`. For example, **balls** and **holes** are represented by a **circles**, **edges** and **hole walls** are represented by **rectangles**, **bumps** are represented by **shapes** where every vertex is individually pin-pointed to the screen. **Angled pieces** are shown as **pixels** where corresponding vertices of a bump have been selected and the vector comprising the vertices has been discretised to find the correct pixels (more on this later).

## Physics
Every "object" of the billiard game, i.e. a shape that interacts with other shapes or is said to have *physics*, gets resolved into two steps when a collision has been found to occur. These two steps are **penetration resolution** and **collision resolution**. Both of these steps  are checked and performed in every simulation step before the objects are rendered to the screen.

The penetration step and collision resolution can be found for every object to object interaction under the Collision System, *collisionSystem.pde*. There are three interactions that need to be simulated to achieve a functioning billiard game, these are **Ball to Ball**, **Ball to Bump** and **Ball to Angled Piece** interactions.

### Ball to Ball Interaction
#### Penetration Resolution
As soon as the balls are found to be intersecting each other, one of the intersecting balls is pushed back to its initial collision position.
#### Collision Resolution
The changes in velocities of the two balls is found using simplistic Newtonian conservation of momentum.

![](images/ballToBall.gif)

### Ball to Bump Interaction
#### Penetration Resolution
#### Collision Resolution
![](images/ballToBump.gif)

### Ball to Angled Piece Interaction



