# Game-33

This project will require you to build a card game – “33” with graphical user interface. The panel can have just results and three buttons to stop or start and deal. If you add more graphical design, you will get extra credit.

“33” is similar to the game of 21 (aka Blackjack) with a few minor revisions. Instead of trying to reach 21, you want to be the closest to 33 without go over. This is a single player game with a dealer.

The basic premise of the game is that you want to have a hand value that is closer to 33 than the dealer, without going over 33. The rules of play for the dealer are strictly dictated, leaving no decisions up to the dealer (aka the computer).
In "33", the cards are valued as follows:

		• An Ace can count as either 1 or 11, as explained below.
		• The cards from 2 through 9 are valued at their face value.
		• The 10, Jack, Queen, and King are all valued at 10.
		• One-eyed Royals (Jack of Spades, Jack of Hearts, and the King of Diamonds) are worth 13
		
In every deal, the card should be removed from the deck. The value of a hand is simply the sum of the point counts of each card in the hand. For example, a hand containing (A,5,7,9) has the value of 32. The Ace can be counted as either 1 or 11. The user and the dealer do not need to specify which value the Ace has. It's assumed to always have the value that makes the best hand. An example will illustrate: Suppose that you have the beginning hand (Ace, 6, 8). This hand can be either 15 or 25. If you stop here, the value of the hand will be 25. Let's assume that you draw another card to the hand and now have (Ace, 6, 8, 2). Your total hand is now 27, counting the Ace as 11. Let's backtrack and assume that you had instead drawn a fourth card (10). The hand is now (Ace, 6, 8, 10) which totals 25. Notice that now the Ace must be counted as only 1 to avoid going over 33.

The dealer must play her hand in a specific way. The dealer must continue to take cards until her total is 26 or greater. An Ace in the dealer's hand is always counted as 11 if possible, without the dealer going over 33. For example, (Ace,8,8) would be 27 and the dealer would stop drawing cards. Also, (Ace,8,7) is 26 and again the dealer will stand. (Ace,8,6) is only 25, so the dealer would get another card. She will continue to draw cards until the hand's value is 26 or more. For example, (Ace,5,8,10) is only 24 so she gets another card. (Ace,5,8,10,2) makes 26 so she would stop and NOT get another card.

The dealer has no choices to make in the play of her hand. She must simply hit until she reaches at least 26 or busts by going over 33.
The player and dealer can also tie. A player can have the same value of cards (“push”) as the dealer. The program should keep track of the wins, losses and pushes. The program should continue until the user wants to quit (Push the Stop button), or she reaches 5 wins. In each play the deck should be created and shuffled.

Design hints:
		
The Project will require you to create five classes: PlayGame, CasinoTable, Card, DeckOfCards and Thirty3:
Design and implement a class called Card that represents a standard playing card. Each card has a suit and face value.
Create a class called DeckOfCards that has an array of Card class. Remember a deck of cards consists of 52 cards (Ace, 2-10, Jack, Queen, King) in four suits (Hearts, Diamonds, Spades and Clubs).

The Thirty3 class, should create a single Deck object that contains all of the cards. The manipulation of the Deck object should be handled within the Deck class. Thirty3 should handle all of the game play. Note: Additional objects may be used

PlayGame.java: the driver class just create the panel
CasinoTable.java: panel
