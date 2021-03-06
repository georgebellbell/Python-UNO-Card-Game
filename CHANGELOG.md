# CHANGELOG
* v1.1.9 [2019-11-28]: Discovered issue where player name dorothy is never implemented due to only the first 3 names in the list being used.
 Fixed this by doing a random.shuffle of the contents of the names so dorothy will have a chance of being picked

*  v1.1.8 [2019-11-26]: Final change made so that all 20 tests pass. Issue with list object has no attribute split has been fixed 
 by removing some unneeded square brackets

* v1.1.8 [2019-11-26]: Issue in function run_player that brings up an assertion error if the stack of card is empty and trying to assign nothing to empty card. 
 Fixed it by including a try and except clause which will only assign a card if there is no assertion error. If there is one then a card will just be
 drawn from deck.

* v1.1.7 [2019-11-25]: More fixes have been made, solving most fails in pytest. Cards now definitely get reshuffled if stock is empty.  

* v1.1.6 [2019-11-24]: A few small fixes which allow more of the pytest functions to succeed, and hence the actual game. 
 Error with wrong card causing draw 2 ability to occur has been fixed

* v1.1.6 [2019-11-24]: Allow game to continue if deck of cards is empty my reshuffling with the discards.
  See work done in  draw_and_discard function with except index error used if main card stack is empty

* v1.1.6 [2019-11-24]: Issue with won index being out of range fixed by placing brackets when determining value for c: c = (c + self.direction) % len(self.players)

* v1.1.5 [2019-11-23]: If player picks card to discard that can't be, i.e when they have no playable cards rather than 
 trying to discard bottom card in hand draws a new card from deck and if discardable does so and if not is added to players hand. 
 Accomplished by setting card variable in draw and discard to self.stock.pop() and then if it couldn't be discarded appended that
  card to the players hand

* v1.1.5 [2019-11-23]: Ability of Jack card now works with next player in order being skipped
   nested majority of code for a turn in run player function so it will only run if that user is not being skipped

* v1.1.4 [2019-11-22]: Effect of King card now works with direction of game being reversed.
  self.direction *= -1 in elif statement for king so direction will alternate between positive and negative. 

* v1.1.3 [2019-11-21]: Base functionality of game works with only discarding cards with matching suite or value to top
value. Accomplished this by changing the can discard function to make sure it returns boolean values and use this to check 
card to discard in run player function

* v1.1.3 [2019-11-21]: Assert fixed in the test_switch.py file
 test_can_discard__allows_ace had assertion of King rather than Ace so made appropriate change

* v1.1.2 [2019-11-20]: Users dealt correct number of card at start.
 Changed value for variable HAND_SIZE from 7 to 8

* v1.1.1 [2019-11-19]: Fixed bug in switch script for order of turns
  Added if statement that sets pointer for who's turn it is back to the first player (0) when end of players list is reached. 
  Also added increment so successfully goes through all players. For switch.py script.
  
* v1.1.1 [2019-11-19]: Fixed bug in players script.
  Simple fix for players.py, line missing closing bracket so has been added

* v1.1.1 [2019-11-19]: Fixed bug preventing game from starting.
  Created and called object called game, the instance of class Switch, outside of the class in the switch.py file

* v1.1.0 [2019-11-08]: Added a SmartAI computer opponent.
  Added strategy players.SmartAI
  None of the bugs have been fixed.

* v1.1.0 [2019-10-25]: First major release.
  This version is known to contain some bugs.

