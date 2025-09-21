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

i forgot how to turn on the AI but i have all the code... what a shame. 
