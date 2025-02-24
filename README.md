Download link :https://programming.engineering/product/homework-1-maze-game-solution/


# Homework-1-Maze-Game-Solution
Homework 1 “Maze” Game Solution
Objectives:

Get your hands dirty coding a (relatively) simple game involving structs, objects, and enums.

Turn In:

A .zip file containing the following: ​main.cpp, Maze.h, Maze.cpp, Player.h, Player.cpp, Makefile

Instructions:

Your job is to implement a “maze” game. The word “maze” is in quotes here because “grid with random walls in it” is more accurate. As you’ll see from this description, in its most basic incarnation, this game can produce “mazes” that aren’t solvable—the player can’t move and the game will never end.

We’ll implement a basic, but forgiving text UI to play our game. You can think of this game as the first things that you would implement if you were trying to implement pacman. There is a single human player who you will ask which direction they want to go each turn, and the player will walk around collecting treasure until they reach the exit.

Here are some screenshots of what our version looks like (see page 4 for a complete run-through on a small board):



Here, the player is the owl, walls are red crosses, treasures are pears, enemies are clown faces, and the exit is the green check mark.

Each turn, the current player should be told which directions are legal moves. Every move that does not go off the board or run into a wall is a legal move.

The current player will earn 100 points each time they collect a treasure.

If an enemy moves onto a square with the human on it, the human is destroyed. If the human moves onto a square with an enemy on it, the human is destroyed.


If an enemy moves to a square with another

enemy, neither player moves and the turn is

forfeited.

The game ends when the player successfully

reaches the exit or the enemies destroy the

human.

Here is an example of an impossible board that was generated since the exit has no path to it (you can’t move diagonally).

The rules for board layout are as follows:

– The player always starts in the upper left corner

– The exit is always in the lower right corner – Walls appear with a 20% chance in the

spaces that are not the beginning space

or the exit

– Treasures appear with a 10% chance in

spaces that are not walls, the beginning

space, or the exit

– You can decide where the enemies start,

so long as they do not start on a wall or

the exit.

Step 1 — the “basic” game (80 points)

We are providing header files and a Makefile. Your job is to implement the guts of the objects and re-create this game. Your display doesn’t need to exactly match ours (use your design and text UI skills as you wish), but the functionality should match ours.

The header files that we provide currently have most of the code commented out. This is so that you can uncomment and implement as you go. You ​should not attempt to implement everything before compiling​.

We recommend that you start with Player, test out the Player object, then move on to Board, then Maze. Most of the functionality in Maze will depend on you having a working Board.

The TakeTurn function in Maze will likely be the last one that you implement, as it will depend on having all the other functions in place and working.

There are screenshots of an entire run-through of the game on the last page of this write-up.

Step 2 — improving the game (5 points)

The game we have described is not ​super​fun, nor is it ​entirely​functional—it’s possible (fairly likely even), that the player can’t even reach the exit. There are no enemies. There is only one kind of treasure. There aren’t any traps.

Once you have implemented the basic game, choose one of the following features to implement:

Ensure that there is always an open path from the player to the exit. For example, you could just generate new boards until one has a path. You should not just generate a board with the edges free of walls or with no walls at all.

Add different kinds of treasure. You should make the new kinds of treasure ​both​have a different appearance from the basic treasure, and have a different point value. (add at least 2 new kinds of treasure)

Add some danger to the board in the form of stationary traps. Make it possible for the player to lose lives and perish before exiting the board. These traps could be large, they could be invisible, they could be made of fire—it is up to you.

Give the player a fixed amount of time or turns to complete the puzzle.

Step 3 — extra credit (15 points)

You cannot get points for extra credit unless you have completed both step 1 and step 2. We highly recommend​choosing #1 the feature that you implement for step 2 if you are doing the extra credit.

Give the enemies strategies so they are computer controlled. If you have multiple enemies, they can all follow the same strategy or different strategies. Extra credit will be scaled on how sophisticated your enemy strategies are.

General guidelines

The program that you turn in ​must compile.​You will receive a hefty deduction for programs that do not compile. Even if your program is incomplete, ​make sure it compiles.

Similarly, the code that you turn in ​must run​. You will get credit for programs that are partially complete, but you will get a hefty deduction for programs that do not run. ​Make sure that it runs. ​We will be testing your code on the vm.

15 points will go to style and comments. Your files and functions should have comments. We should know how to run your program and how to use your functions from your comments.

Your variables should have meaningful names. Your code should be easily readable. If you have complex sections of code, you should use inline comments to clarify. You should follow the style guidelines posted on our course github.

As a reference, our Maze.cpp about 350 lines, our Player.cpp is about 40 lines, and our main.cpp is 25 lines (all counts including whitespace and comments).

Happy coding and remember to post questions on piazza!

The example to the left shows a complete right through of the game.

The user’s choice is case insensitive. If they enter an invalid option, they are prompted again.

Once the user steps onto a space with a treasure, that treasure should be collected — the user should have 100 more points and the treasure should disappear.


The human player earns 1 point for successfully getting to the exit.

When the game ends, it should report how many points each player has.

CSCI 3010 — — Muzny — Homework 1

5



 
