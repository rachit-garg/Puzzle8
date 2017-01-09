# Puzzle8
our of the code

The starter code for this activity is composed of four classes:

PuzzleActivity which is the lone activity for this program:
onCreate: in addition to the boilerplate, the given implementation programmatically adds the PuzzleBoardView object to the UI.
onCreateOptionsMenu, onOptionsItemSelected: just boilerplate
dispatchTakePictureIntent: handler for the Take Photo button
onActivityResult: handler for the system call when the photo taking is complete.
shuffleImage and solve: trivial handlers for the other two buttons
PuzzleBoardView, a custom View responsible for drawing the puzzle on screen
PuzzleBoardView: Constructor. Given implementation is complete.
initialize: to add a picture to the view.
onDraw: called by the system when the view should be redrawn. Note the code that will animate the solution once you implement the solver.
shuffle: the actual handler for the "Shuffle" button. You will need to implement this.
onTouchEvent: code that handles user clicks
solve: where your solver code will go
PuzzleBoard which represent the state of the puzzle. This class is separate from PuzzleBoardView because there will always be only one PuzzleBoardView but we will deal with multiple PuzzleBoard objects when we implement the shuffle and solve functionality
NEIGHBOUR_COORDS: a constant array storing the relative coords of all the neighbors of one tile. This will make possible to check neighbors with a for-loop rather than 4 if-statements.
PuzzleBoard: Constructor. This should handle breaking up the given image into tile-sized chunks.
PuzzleBoard: Copy constructor. This constructor creates a puzzle board that copies the state of another puzzle board. This will be handy when implementing neighbors below.
reset: Part of the solver functionality
equals: Tests whether two boards are equal by checking whether their tile configuration is the same.
draw: Called by PuzzleBoardView's onDraw. Makes each tile draw itself.
click: Called by PuzzleBoardView's onTouchEvent. Determines which tile was clicked and attempts to move it.
tryMoving: helper for click.
resolved: Checks whether the current board is solved. This is the reason why we store indexes in each tile.
XYtoIndex: helper method to convert between two-dimensional coordinates and positions in the ArrayList.
swapTiles: private helper. Does what it says.
neighbours: will create a list of all board configurations that can be reached by moving a single tile in the current board.
priority: computes the priority of the current board. This will be explained as part of the instructions for the solver.
PuzzleTile which represents a single tile. This is fully implemented for you.
PuzzleTile: Simple constructor that stores the given index and bitmap.
getNumber: Getter for the tile index.
draw: Draws the bitmap on the given canvas at the given location.
isClicked: Determines whether the touch location falls within the tile.
