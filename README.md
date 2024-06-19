This game creates moving targets on the screen that the player needs to click on. Targets appear at random positions and grow until clicked or they disappear. The game tracks time, accuracy, and speed of clicking targets.

## Features
Targets appear randomly on the screen.
Targets grow and shrink continuously.
Tracks time elapsed, hits, misses, and accuracy.
Game ends when the player misses a certain number of targets.

## Prerequisites
Python 3.x
Pygame library (pip install pygame)




```Target```:

Represents a target object that appears on the screen.
```__init__(self, x, y)```: Initializes a target at position (x, y).
```update(self)```: Updates the size of the target, making it grow until it reaches its maximum size and then shrink.
```draw(self, win)```: Draws the target on the window win.
```collide(self, x, y)```: Checks if the point (x, y) collides with the target.

```draw(win, targets)``` : Draws all targets in the targets list on the window win.

```format_time(secs)``` :Formats a time duration given in seconds into a string in the format MM:SS.ms.

```draw_top_bar(win, elapsed_time, target_pressed, misses)``` : Draws the top bar of the game window with information about elapsed time, speed, hits, and remaining lives.

```end_screen(win, elapsed_time, target_pressed, clicks)``` : Displays the end screen with final statistics like total time, speed, hits, and accuracy. Allows the user to quit the game by pressing any key.

```get_middle(surface)``` :  Returns the x-coordinate of the center of surface relative to the game window.

```main()``` : Main game loop that initializes Pygame, manages targets, tracks game state (time, hits, misses), and handles user input. Ends the game and displays the end screen when the player misses too many targets.
