# BattleshipGame

This application is a two player Battleship game implemented in Java Swing. The user(you) will play the battleship game against the computer. The game consists of two grids - one for the user and one for the computer. Battleships of different sizes are placed on the grid either vertically or horizontally. The ships can occupy more than one grid position. For example, a ship of size 3 will occupy 3 grid positions. It is required that all ships are placed within the limits of the grid which implies that you cannot have ships sticking out of the grid.

<h2>General rules of the game</h2>
Every player has knowledge about the positions of his/her ships but does not have any knowledge about the positions of the opponent's ships. The objective of the game is to shoot down all the ships of the opponent. To shoot down a ship, all the grid locations occupied by the ship must be fired upon. During a turn, a player will pick a target on the opponent's grid. The opponent's grid will then be marked to indicate if it is a hit or a miss. Both players take turns until one of the players is able to successfully shoot all of the opponent's ships. The first player to shoot down all their opponent's ships is the winner.

<h2>Customizations</h2>
For convenience, the user's ships are randomly placed on the grid and their positions are indicated with a blue color. This way the user does not have to place the ships and can play the game right away. The computer ships are also placed randomly on the computer field but they are not shown.

The user will start the game by firing on computer's grid which is accomplished by clicking on one of the buttons on the computer grid with his/her mouse. The grid button will indicate whether it is a hit(red) or a miss(black). The computer will then fire upon the user's field immediately and the corresponding grid button on the user field will turn red if it is a hit and black if it is a miss. The computer will automatically fire on the user field and there is no action required on behalf of the user. The user and the computer will take turns until either the user or the computer is declared as the winner.

<h2>Computer Strategy</h2>
The user moves are made by the person who is handling the mouse. However, computer moves follow a strategy. The computer strategy involves building a list of unexplored candidates around a previously hit target. If a location was hit, the computer adds four of its neighbors(top, left, bottom, and right) to a list of candidates. It will also ensure that none of these candidates were previously picked. So, the next time it needs to pick a location, it will pick one from this list of candidates. This will allow the computer to pick smarter grid locations instead of random ones. Here is the algorithm used by the computer to pick the next location to fire upon:
<ol>
    <li> If list of candidates is empty and previous strike was not successful </li>
        - pick an unexplored random location. 
<li> Otherwise 
    <ol>
        <li> If previous strike was successful </li>
            - Add unexplored neighbors of the hit location to list of candidates.
        <li> If list of candidates is not empty</li>
            - pick the first candidate in the list. <br>
        Otherwise <br>
            - pick an unexplored random location.
    </ol>
    </li>
</ol>
<h2>Running the application</h2>

To run the application issue the following command on the command line:

<b>java -jar Battleship.jar </b>

When the application runs, click on "File" menu at the top left corner of the window and select "New Game". This will setup the game by showing both grids. You will also see some grids on the user field marked with blue color showing the placement of ships on the user's grid. Start playing the game by clicking on any button on the computer field. The computer will immediately respond by making its move. Continue playing until a winner emerges. You can start a new game anytime you want.

To obtain the individual class files of the application, you can issue the command:

<b>jar tf Battleship.jar </b>

This jar file was created using the instructions listed here: <br>
https://docs.oracle.com/javase/tutorial/deployment/jar/appman.html <br>
This page explains how to create an application's entry point.

