# Conveyor
Godot game

# MVP

### Arcade Mode

Incomplete blocks start on the left side of the screen and move down a coveyor belt to the right of the screen.
The players objective is to complete the blocks by placing parts into the empty spots of the block. If all empty spots
are filled by the time the block meets the end of the conveyor the block is scored. If any empty spots still remain
once the block meets the end of the conveyor the block is not scored.

1. Blocks
  * ~~2x2, 3x3 or~~ 4x4 grid
  * Created from parts
  * Starts partially filled; solid blocks are...solid, empty spots in blocks are surround by a dotted line
  * Max 3 on belt
  * Have empty spaces that can be filled with parts - should have set of predefine incomplete blocks for MVP
  * scoring complete +1pt
  * scoring incomplete -1pt

2. Parts
  * 4 part types
    single square
    three long 3x1
    corner L
    Tee T
  * Place into blocks, one at a time
  * Picked up & rotated, one at a time
  * Can be placed back into parts bin

3. Parts bin
  * infinite amount of four  part types

4. Conveyor belt
  * Moves blocks to scoring area
  * Holds 3 blocks at a time
  * Blocks are added one at a time (One off One on)

5. Placement rules
  * Part must fit into available space
  * Parts can hang out of block -for some negative scoring?
  * Parts cannot overlap existing parts in the block

# Pieces system

### Piece
- Represents 1x1 square
boolean exists = false;

### Form extends Piece
- array of pieces
extends Piece
boolean[] Form = new array<boolean>[12]
This array can be used to represent the form and allow for parts to be rotated
and stil be compared to Blocks with the correct orientation.

Visualiztion of Form array:
[ 1 ][ 2 ][ 3 ][ 4 ]
[ 12][ 13][ 14][ 5 ]
[ 11][ 16][ 15][ 6 ]
[ 10][ 9 ][ 8 ][ 7 ]

  * indices represent 4 sides of form

### Part extends Form


### Block extends Form





