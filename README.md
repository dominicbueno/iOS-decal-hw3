# iOS-decal-hw3

## Space Fighter ##
## Authors ##
  * Dominic Bueno
  

## Purpose ##
  Play as a heroric space pilot fighter in an endless journey through space.
## Features ##
  * Procedurally produce terrain for pilot to navigate through. Update score based on time and targets destroyed. Unlock upgrades as you build your score.
  
## Control Flow ##
  * Upon opening the app the user is introduced to the main menu. 
  * The menu will contain a start game button, high score button and unlock button. 
  * Start game will initiate the game. 
  * High score will show the top 3 highest scores of the user.
  * The unlock screen will contain upgrades the user can get for their ship using their score as currency. 
  
## Implementation
### Model ###
   * GameLogic.swift - This file will control game logic such as scores and unlocks and will be used through the 3 views.
   * ProceduralGenerate.swift - randomly generates adversaries, difficulty increases over time.
   
   
### View ###
   * MenuView - This view is a gateway to the other views and will contain 3 buttons that will show the other views
   * GameView - This is the view of the actual game. This is where the hero and his adversaries appear.
   * HighScoreTableView - A simple table view of top 3 scores.
   * UnlocksTableView - A table view with the unlocks and price, the cells in the table will be custom
   
   
### Controller ###
   * GameViewController - Uses GameLogic.swift to determine things like score. This controller will be responsible for making entities appear on screen using ProceduralGenerate.swift. The controls will also be implemented in this controller using touchesBegan and getting the touch location.
