# glass_lake (seriously-WIP)

an abstraction for an interaction in time, based on Ludics

high-level theses:

- equivalence between PROOFS, PROGRAMS (Curry-Howard Isomorphism), but also DIALOGUES, GAMES and INTERACTIONS IN GENERAL
- equivalence between normalization and reduction, i.e. the execution of a program (Curry-Howard Isomorphism), as well as 'cut-elimination'
- an interaction proceeds by a DESIGN, a sequence of proofs and counter-proofs (strategies)
- not governed by a gain/success/win function, instead the game ends when players reach a situation where one of them endorses the move made by the other
- language IS cut-elimination/normalization/reduction

general elements:

- two sequences of moves, one for each player (players A and B)
- each step has two actions, a positive and a negative one
- players take turns alternating between taking positive and negative actions (+, -)

step/move:

- polarity (negative or positive action)
- address (sequence of integers, each representing the locations leading up to present one)
- ramifications (set of addresses that can be reached in one step)

positive action:

- a positive action involves laying down an array of locations/cards, each represented by an 'address' for that location  ([ 1.1, 1.2, 1.3 ]). these are known as 'ramifications'
- there is another type of positive action called the 'daimon', that ends the game/interaction
- a player taking a positive action is known as the 'proponent'

ramifications:

- ramifications are the addresses representing the points being made by the player, or the questions being asked
- these are 'cards' being laid down by the player
- these are the addresses that can be reached in one step
- (point of confusion: are these the questions or the possible answers to questions?)

negative action:

- a negative action involves the other player 'searching' their 'deck' for 'cards' that may correspond with the cards laid down by the positive player
- note that this is NOT the player in the negative position laying down the card. the player in the negative position can lay down the card in the next step or turn
- a player taking a negative action is known as the 'opponent'

convergence/normalization (intra-step):

- this occurs when the player in the negative position can 'find' a card of corresponding polarity to one of those laid down by the player in the positive position

convergence/normalization (big-step):

- this occurs when ALL cards have been eliminated, that is, all cards of positive polarity have been matched by corresponding cards of negative polarity
- in other words, all questions have been answered, all assertions addressed (assented/dissented)
