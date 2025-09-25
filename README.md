Senen Bagos III
9/20/2025

as i was making it I tried to leave whwre the given comments were so it's easier for me to follow the steps. thats what i did in cst325

turns out i didnt need to make an update function.... anyway thats why you read right? ill leave it in there to show for it 

setUpBoard()
i was having a brainfart trying to make the grid. idky i thought i had to initialize a square for the grid even tho it already was and i could just call the method but i figured it out. that was the first hump.


stopGame()
after i got over the initial hump this method was very self explanatory 

ownerAt()
checks what quadrant is owned by whom 

checkForWinner()
checks if an owner owns a winning combo by getting the owner of the winning combo (like 0, 1, 2) and making sure its the same owners, if not go to the next winning combo

checkForDraw()
if there is no winner yet, check if all the squares are filled, if so return true, else keep playing

state Strings() 
they were heavily documented so it was easier to follow along

AI: Negamax and Alpha Beta Pruning

isAIBoardFull()
checks if the state string has no 0 char, if true ends the game

checkForAIWinner()
goes through all winning combos to see if the same player owns a winning combo, if so return 10, else return 0

updateAI()
gets the current state string, finds an open square and places a temp 2 then calls negamax to check the move. When it's done resets it back to 0. It then checks what move gave it the highest score, storing it in bestSquare. When the best square is chosen, the AI makes its move then ends turn.

negamax()
state -> the current searching state
depth -> the far in the search we are
alpha, beta -> pruning values to cut off useless searching early
playercolor -> which player is moving

checks if its a terminal state, if there is a winner, return a -score, which is bad for the parents node 

if board is full, return a 0 

it introduce a value that the current player has to beat.

goes through all empty squares, and places the current players piece, 1 or 2, 
calls itself recursively to flip between the two, then undos the move, 
use alpha beta to remove useless branches to save time. 
returns the best score from the current state.

theres a min (human) and max (AI) player, and each player wants the best score in their regards. 
when ever negamax is called it flips between the two (also flipping alpha beta), technically making the current player "maximize" their own score. 

for example, if a child node wins that means the parent lost. This will happen by seeing if a player has a winning combo. this technically means its searching for the best move, then puts it at that spot to prevent it if the opposing play can win
