Download Link: https://assignmentchef.com/product/solved-csci235-project-4-a-game-that-provides-a-series-of-levels
<br>
The game provides a series of levels. In each level, the user controls a character (representing the game player) which must collect treasures and avoid monsters. The character is controlled by five buttons: to move up, down, left, and right, and to disappear or reappear. The monsters will move toward the player (the character on the grid), and if one “gets” the player, the game is over. The player collects treasures by moving into a space that currently holds a treasure. When all treasures in a level are collected, the level is cleared and the player moves on to the next level. When all levels are completed, the game is won. The

initial screen of the game looks like as follows:

The green ‘P’ stands for the player.

The yellow ‘O’ stands for the treasure.

The magenta ‘M’ stands for the monster.




<strong> </strong>

<strong> </strong>

The “Disappear (or Reappear)” button makes the player appear or disappear. The advantage of disappearing is that the monsters cannot see the player (but they can still get the player if they happen to move into the player, or if the player happens to move into them while the player is invisible). The disadvantage is that the player character (“P”) is invisible and cannot collect any treasure.

In the lower levels, the monsters will stop moving if they don’t see the player, but in the higher levels, they will remember where the player were and keep moving toward that spot.




To play the game, compile <sub>Player.java</sub> and run either

java –cp .<strong>:</strong>game.jar MonsterGame  (if your system is Linux or Mac)




or

java –cp .<strong>;</strong>game.jar MonsterGame (if your system is Windows)




The buttons currently don’t work. You will write the methods of the Player class to make those buttons work.










1 <strong>The Player class’s contract </strong>with the rest of the game program is as follows:

<ul>

 <li>It is given an initial location (<sub>int</sub> x and y coordinates in the grid) and the size of the grid <u>in its</u> <u>constructor</u>. The current constructor does nothing with this information.</li>

 <li>It needs to report its current location when the methods <sub>getXPos() </sub>and <sub>getYPos()</sub> are called. Currently these methods always say the player is in position (0, 0). You should update those statements.</li>

 <li>When the user clicks on the appropriate button, the method <sub>up()</sub>, <sub>down()</sub>, <sub>left()</sub>, <sub>right()</sub>, and <sub>disOrReappear()</sub> are invoked on the object.</li>

 <li>When the method <sub>getIcon() </sub>is called, it must return a character. If the player is visible, the character returned will represent the player on the screen; if the player is invisible, it should return a space character. Currently, it always returns the letter ‘P’ (for the player).</li>

</ul>




Your task is to finish this class, <strong>according to the above contract</strong>. You should think about:

<ul>

 <li>What information this object (a Player object) needs to store (this will help you <u>determine what</u> <u>the instance variables should be</u>).</li>

</ul>

o    Figure out necessary instance variables first. Hint: recall that the constructor initializes instance variables by using the values delivered by the formal parameters.

<ul>

 <li>What the methods getXPos(), getYPos(), and getIcon() should return, based on the values of the instance variables.</li>

 <li>How the methods up(), down(), left(), right(), and disOrReappear() affect the instance variables.</li>

</ul>

Grid positions are numbered starting at zero, increasing toward the right and toward the top. <u>You are</u> <u>responsible to make sure</u> that if the user clicks (for example) the left button when the player is already on the left edge of the board, then the player does not actually move any farther left. Otherwise the program will crash.

Your code should NOT include any particular value (i.e., 5 or 30) for the size of grid or the position of the Player object.