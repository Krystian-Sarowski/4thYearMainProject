# 4thYearMainProject

Main project on which I have worked on through the entirety of 4th year.
The focus of this project was to develope a demo of 3D Rogue-like game using unity.

The levels within this game are generated using two different approaches referred to as Bottom-up and Top-down.

In the Bottom-up approach I place the rooms randomly within the level area and create arcs between each room
that is in a straight line to another room. I then create a Minimum Spanning Tree using these arcs to connect
each room using the shortest arc each time.

In the Top-down approach I place down each room using Recursive-subdivision dividing the level area each time 
a room is placed. This creates a Binary tree that I then use to connect each room from the left nodes with 
each room from the right nodes choosing the closest pair each time starting from the bottom of the tree.

The result of either of the two approaches is then converted into a 3D mesh by creating a 2D celling mesh 
selecting which tiles are counted as wall tiles and then extruding a vertical mesh of the walls choosing
by choosing the lines in the 2D celling mesh that are used only by one triangle.

In each combat room there are enemies that traverse the room using the wander algorithm and avoid obstacles
using raycasting.