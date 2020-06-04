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
- array of pieces used to represent Parts and Blocks
Piece[] Form = new array<Piece>[12]
This array can be used to represent the form and allow for parts to be rotated
and still be compared to Blocks with the correct orientation.

Visualiztion of Form array:
[ 1 ][ 2 ][ 3 ][ 4 ]\
[ 12][ 13][ 14][ 5 ]\
[ 11][ 16][ 15][ 6 ]\
[ 10][ 9 ][ 8 ][ 7 ]\

  * indices represent Pieces in Form
  * Iterating over Pieces in the Form of a Part and Block will allow for comparison
  of overall shape that exists in each. This can be used to determine if a Part (in any orientation)
  can be placed in empty Pieces of a Block.
  *Will need to find a way to compare a Part and Block when the Part's Form 
  would be offset from the Block's Form

### Part extends Form
- int topLeft
    * Starting index for part orientation and comparison
    * Parts can be rotated and topLeft can change to represent new orientation
    * topLeft will be 0,3,7 or 9

### Block extends Form
    * Blocks do not rotate so start will always be at 0




