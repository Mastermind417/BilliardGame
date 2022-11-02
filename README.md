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

Each billiard piece is represented by primitive shapes in `Processing`. For example, balls and holes are represented by a circles, edges and hole walls are represented by rectangles, bumps are represented by a shape where every vertex is individually pin-pointed to the screen. Angled pieces are shown as pixels where corresponding vertices of a bump have been selected. To find the pixels, the vector comprising the angled piece's vertices is discretised (more on this later).




