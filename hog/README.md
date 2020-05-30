# [Project 1: The Game of Hog](https://cs61a.org/proj/hog/)

Develop a simulator and multiple strategies for the dice game Hog. You will need to use control statements and higher-order functions together, as described in [Sections 1.2 through 1.6 of Composing Programs](http://composingprograms.com/pages/16-higher-order-functions.html).

## Run
To play Hog, in the terminal (I used Git Bash) type this command:
python hog_gui.py 

Select the test file in the tests package, right click, and then select Run.

## Files modified or created
- [hog.py](hog.py)

## Tests
Tests are done with the ok autograder:

To run all tests, in the terminal (I used Git Bash) type this command:
python ok

## Game Rules
In Hog, two players alternate turns trying to be the first to end a turn with at least 100 total points. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes. However, a player who rolls too many dice risks:

Pig Out. If any of the dice outcomes is a 1, the current player's score for the turn is 1.

In a normal game of Hog, those are all the rules. To spice up the game, we'll include some special rules:

Free Bacon. A player who chooses to roll zero dice scores points equal to one more than the absolute alternating difference of the digits of the opponent's score cubed.

Feral Hogs. If the number of dice you roll is exactly 2 away (absolute difference) from the number of points you scored on the previous turn, you get 3 extra points for the turn. Treat the turn before the first turn as scoring 0 points. Do not take into account any previous feral hog bonuses or swine swap (next rule) when calculating the number of points scored the previous turn.

Swine Swap. Define the excitement of the game to be three to the power of the sum of the players' scores. After points for the turn are added to the current player's score, if the excitement's first digit and last digit are the same, the scores should be swapped.
