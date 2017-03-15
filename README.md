# glass_lake

an abstraction for an interaction in time

elements

- a public, global gameboard transparent and accessible to both players at all times
- twp players taking turns to commit positive actions
- a positive action is always a possible update to the gameboard
- a private gameboard for each player, restricted to that player

gameboard

- a gameboard is an array of (addresses of) locations, of any number, each location/address representing a possibility
- a gameboard persists through steps, and is referred to simply as 'state' within each step

progression

- two sequences of actions, representing two agents
- each pair of actions constitutes a step
- one action will be considered positive, the other negative
- all gameboards (public, private, private) are passed from one step to the next

positiveAction ('talking')

- assertion (intent to update public gameboard)
- question (invitation to other player to update public gameboard)
- agreement (update of public gameboard)
- denial (denying update of public gameboard)

negativeAction ('listening')

- recording (update of private gameboard with other player's assertion)
- searching (searching private gameboard in response to other player's question)
