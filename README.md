# glass_lake

an abstraction for an interaction in time, based on Ludics

high-level theses:

- the fundamental nature of language is interaction
- equivalence between proofs and programs (Curry-Howard Isomorphism), but also DIALOGUES and GAMES
- equivalence between normalization and reduction, i.e. the execution of a program (Curry-Howard Isomorphism)
- an interaction proceeds by a DESIGN, a sequence of proofs and counter-proofs (strategies)
- no a priori rules
- not governed by a gain/success/win function, instead the game ends when players reach a situation where one of them endorses the move made by the other
- language IS cut-elimination/normalization/reduction

general elements:

- two sequences of steps, one for each player (players A and B)
- each step has two actions, a positive and a negative one
- players take turns alternating between taking positive and negative actions (+, -)

positive action:

- a positive action involves laying down an array of locations/cards, each represented by an 'address' for that location  ([ 1.1, 1.2, 1.3 ]). these are known as 'ramifications'
- there is another type of positive action called the 'daimon', that ends the game/interaction

ramifications:

- ramifications are the addresses representing the points being made by the player, or the questions being asked (these are 'cards' being laid down by the player)

negative action:

- a negative action involves the other player 'searching' their 'deck' for 'cards' that may correspond with the cards laid down by the positive player

convergence/normalization (intra-step):

- this occurs when the player in the negative position can 'find' a card of corresponding polarity to one of those laid down by the player in the positive position

convergence/normalization (big-step):

- this occurs when ALL cards have been eliminated, that is, all cards of positive polarity have been matched by corresponding cards of negative polarity
