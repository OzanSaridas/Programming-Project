# Programming-Project
The first part of the program is the initializing of all 100 cards into an ArrayList called _deck_. I do this utilising for loops to avoid copy and pasting instructions redundantly, and add if loops to make sure 0 is only added once per colour, not twice. 
After this, a while loop that terminates if a boolean called GameRestart = false is implemented, and the rest of the program from here is nested in this loop. This will be used later when the player will have tbe option to restart the game or not
The second part of the program is the shuffling of the ArrayList _deck_ into a new ArrayList called _updDeck_. I shuffle it by utilising a random number generator (RNG), taking the index that corresponds to the random number from the ArrayList _deck_, and adding the card to the ArrayList _updDeck_. The reason this step is nested within the GameRestart loop is so, if the game is restarted, the deck will be reshuffled
The player is asked whether he would like to play against another player or an AI.
**If the player chooses to play against another player, the next part of the code executes:**
  Two ArrayLists, each corresponding to a player's hand, are initialized
  Each player is given 7 cards from the top of the shuffled deck
  The first normal card (a colour and a number) is taken from the top of the shuffled deck and then put on the discard pile, represented by the ArrayList _discardPile_ 
**The following code is used for both player1 and player2, only with variables changed.**
    Two boolean variables are initialised. The first, player1turn, will be used in a while loop containing all the code for the first player. once the code ends,     player1turn will be changed to false and the loop will terminate, which will change the turn to the second player. The second, gameFinish, will nest the entire code for the player vs player program, and will terminate the code once the game is finished.
  Next, the player is given information about the current discard pile and his hand, which allows him to make an informed decision
  An if statement nested within a for loop is used to find cards that are eligible for the player to play, which are then added to the ArrayList _eligible_
  if there are no eligible cards, the player automatically draws and the turn is changed to the other player. otherwise, the player is prompted to enter a card to play. If the card isn't found in the eligible ArrayList, the player is prompted to enter a valid card. Once a valid card is inputted, it is added to the discard pile and removed from the player's hand.
  For loops and if statements are utilised to accomodate unique cards, namely wild cards (including draw four wild cards), skip cards, and draw 2 cards
  At the end of the code, player1turn is set to false, which terminates the loop and allows the second player to play.

  Additional: an if statement between the player1turn loop and the !player1turn loop checks if the player has no cards left. If he has no cards left, he wins and the gameFinish loop is terminated, allowing the player to choose whether he wants to play again or not, which will restart the program if chosen

  **If the player chooses to play against an AI, the next part of the code executes:**
  Two boolean variables are initialised. The first, playerTurn, will be used in a while loop containing all the code for the player. once the code ends,     playerTurn will be changed to false and the loop will terminate, which will change the turn to the AI. The second, gameFinish, will nest the entire code for the player vs AI program, and will terminate the code once the game is finished.
    Next, the player is given information about the current discard pile and his hand, which allows him to make an informed decision
    **The following code is the exact same one used for the player vs player program, only with variables changed.**

**The following code is used for the AI**
  The code is the exact same as the other codes, except this time, instead of prompting the AI to make choices (such as which card to play, or what colour to change the wild card to), the choice is made using a random number generator.

  At the very end of the code, once the game is finished and the gameFinish loop is terminated, the player is given the option to play again, if the player chooses not to play again, GameRestart is set to false and the program ends. If the player chooses to play again, GameRestart is set to true, which will restart the entire program. 
