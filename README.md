# BattleshipGame

This application is a two player Battleship game implemented in Java Swing. The user will play the battleship game against the computer. The game consists of two grids - one for the user and one for the computer. Battleships of different sizes are placed on the grid either vertically or horizontally. The ships can occupy more than one grid position. For example, a ship of size 3 will occupy 3 grid positions. 

A player has knowledge about the positions of his/her ships but does not have any knowledge about the positions of the opponent's ships. The objective of the game is to shoot down all the ships of the opponent. To shoot down a ship, all the grid locations occupied by the ship must be fired upon. During a turn, a player will pick a target on the opponent's grid. The opponent's grid will then be marked to indicate if it is a hit or a miss. Both players take turns until one of the players is able to successfully shoot all of the opponent's ships. The first player to shoot down all their opponent's ships is the winner.

For convenience, the user's ship are randomly placed on the grid and their position is indicated with a blue color. This way the user does not have to place the ship and can play the game right away. The computer ships are also placed randomly on the computer field but they are not shown.

The user will start the game by firing on computer's grid by clicking on the computer grid with his/her mouse. The grid button will indicate whether it is a hit(red) or a miss(black). The computer will then fire upon the user's field immediately and the corresponding grid button will turn red if its a hit and black if it is a miss. The user and the computer take turns until either the user or the computer is declared as the winner.

Computer Strategy:
The user moves are made by the person who is handling the mouse. However, the moves made by the computer involve a strategy. The computer strategy involves building a list of candidates around a previously hit target. If a location was a hit, then the computer picks four of its neighbors - top, left, bottom, and right as candidates. So, the next time it needs to pick a target, it will pick one of these four candidates. This will allow the computer to pick smarter targets instead of random ones.
a) Pick a random target to fire upon if there are no known candidates to fire upon and previous strike was not successful.
b) If the previous strike was successful or there are candidates to explore:
    i) If previous strike was successful 
            Build new candidates around that location.
    ii) If there are candidates to explore, 
            pick one of the candidates to fire upon next.
        Otherwise
            pick a random target to fire upon.

Running the application:

To run the application issue the following command on the command line:

java -jar Battleship.jar

When the application runs, click on "File" menu on top left corner and select "New Game".

This will start the game showing the placement of the ships on the 

To obtain the individual class files of the application, you can issue the command:

jar tf Battleship.jar

