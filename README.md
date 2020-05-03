# Conveyor
Godot game

# MVP

### Arcade Mode

1. Blocks
  * 2x2, 3x3 or 4x4 grid
  * Created from parts
  * Starts partially filled; solid blocks are...solid, empty blocks are surround by a dotted line
  * Max 3 on belt
  * Have empty spaces that can be filled with parts
  * scoring complete -1pt
  * scoring incomplete +1pt

2. Parts
  * 4 part types
    single square 1x1
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
  * Blocks are added on at a time (One off One on)

5. Placement rules
  * Part must fit into available space
  * Parts can hang out of block for some negative scoring
  * Parts cannot overlap existing parts in the block

# Pieces system

### Piece
- Represents 1x1 square
boolean exists = false;

### Form extends Piece
- array of pieces
extends Piece
boolean[] bottom = new array<boolean>[4]
  * indices represent 4 sides of form

### Part extends Form


### Block extends Form





