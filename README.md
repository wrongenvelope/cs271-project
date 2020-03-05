# Final Project in MASM x86
## Game Development Option

### Authors:    Kingsley Chukwu and Heather DiRuscio
### Game:    Blackjack in Space
### Submitted:    March 6, 2020

CS 271
Oregon State University,
Winter 2020 Term

### Description:
The game is a simple implementation of blackjack, where the user is the Player, and you play against the computer, which operates as the Dealer. As the Player, you can choose to Hit or Stand on each turn. Hit will result in another card being drawn from the deck of 52, and added to your hand. The gameboard will then redisplay, showing you all of your cards and your new hand subtotal. At this point, your hand will also be evaluated to see if you have achieved Blackjack or gone Bust. Getting 21 points earns you Blackjack and you will get a point, while ending with 22 points or more is Bust and the Dealer will get a point. The cards don't appear to have suits, but there are four of each card value, like a typical deck.

During gameplay of a hand, you can only see your whole hand and subtotal, and one of the Dealer's cards will appear to be face down. You do not know the value of the Dealer's hand. The Dealer has its own set of behaviors, and will choose whether to Hit or Stand without input from the Player. If you manage to get 10 points (win 10 hands) first, you win, and can take off to explore space! However, if you fail to get 10 points (win 10 hands) before the Dealer does, you will lose the game... and face an uncertain fate.

### Procedures:
1. Main Procedure - drives other procedures
2. Title_Screen - displays graphical title screen
3. Start_Game - initialize player/dealer points to 0
4. Start_Hand - empty player/dealer hands, reset card deck
5. Draw_Card - add one card to player or dealer hand
6. Evaluate_Hand - evaluate sum of points values for all cards in one hand
7. Show_Game - set up "gameboard" display with scorebox
8.	Check_Win - check for blackjack/bust conditions
9.	Print_Hand - print out all cards from one hand in a row
10.	Face_Cards - helper procedure to display value on face cards
11. Card_Spacer - helper procedure to space cards from left edge of terminal
12.  Player_Turn - player can choose to Hit or Stand
13.	Dealer_Turn - dealer will decide to Hit or Stand
14.	Pick_Winner - if both player and dealer Stand, see who has more points
15.  Game_Over - display won or lost game screen
16. Exit_Blackjack - prompt player to play again or quit

### Known issues:
1. Sometimes, Ace cards appear with @ symbol or = symbol instead of expected value "A"
2. The dealer's full hand (including face-down card) is not always revealed at the end of a hand. It works as intended if a player chooses to Stand, but the flags aren't set correctly if they choose Hit.
3. In hands with multiple Aces where the value of the Ace would be reduced from 11 to 1, only one Ace might be counted. (E.g. a hand with A, 2, A would have a value of 3 instead of 4)
4. Player hands that bust are frequently evaluated to "30" instead of their actual points value. The determination of whether someone has Bust seems correct, but the ending value displayed is not.

### Feature Wishlist:
1. A betting system
2. More space-themed stuff (the dealer is supposed to be an alien)
3. Display things on the screen without scrolling, i.e. clear the screen and redisplay after drawing a card
4. Suits to display on cards
5. Additional input validation
