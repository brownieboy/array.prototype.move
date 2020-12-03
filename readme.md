# Array.protoype.move

Array method to move an element of that array from one index to another.  Extends the Array.prototype to add the move method.  It will check for an existing move method first.


## Installation
Install from npm, like so:

    npm install array.prototype.move --save


## Importing
Simply require or import the file.  There's no function exported, so no variable to assign to on the import/require.  The code modifies the Array.prototype via an IFFE (Immediately Invoked Function Expression).

Import/require like so:

    import 'array.prototype.move';   	// ES6 syntax
    require('array.prototype.move');	// CommonJS syntax

You can also add it as a simple script tag if you're not using any module loaders.  The file to load in that case is array-prototype-move.js, which you'll find in the /src folder.

## Syntax
The syntax is:

    myArray.move(moveFromPosition, moveToPosition)

where:
* `myArray` is your array.  It can be an array of objects, as well as an array of primitives (strings, numbers etc).
* `moveFromPosition` is the index of the array element that you want to move, where zero is the first element.
* `moveToPosition` is the index of the array where you want the element that you're moving to end up.

Example 1:

    var simpleArray = ["Han Solo", "Luke Skywalker", "C3P0", "R2D2"];
    simpleArray.move(3, 0);

will move R2 to the start of the array.

The method will also accept negative numbers for either of the "move" variables.  In that case, -1 is the last element of the array, -2 is the next to last element, and so on.

Example 2:

    var simpleArray = ["Han Solo", "Luke Skywalker", "C3P0", "R2D2"];
    simpleArray.move(0, -1);

will move Han to the end of the array.


## Development
As usual, after cloning the repository, install the required packages like so:

    cd array.prototype.move
    npm install

There is no build step.  Edit the one source file in the /src folder.  That's the distribution folder too!  (The *main* entry in the package.json file points to there.)

To run the test suite.

    npm test


## Acknowlegements
Taken from Reid's accepted answer from [the most popular stackoverlow post on this topic](http://stackoverflow.com/questions/5306680/move-an-array-element-from-one-array-position-to-another).  All credit goes to Reid.  I've not changed his code at all.

