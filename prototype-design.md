# Prototype Design Doc Idea 

 
## Basic User Experience Outline

1. Web Landing page is start button with intro to game concept “Escape the code! Learn to code by solving code puzzles that will introduce you to programming concepts in the language of your choice! One challenge at a time!” 
2. User clicks start 
3. Enters username 
4. Selects programming language 
  - Python, Node.js, Java, .NET 
5. Selects difficulty of programming concepts 
  - Beginner, Intermediate, Advanced 
6. Next page is the start of the game. A 2d restaurant/kitchen room representation  
  - Three rooms – Garden, Kitchen, Dining room  
  - Multiple challenges in each room 
    - Max of 3 challenges per room 
7. User clicks on different parts of the room and is prompted with a challenge that is based on a programming concept to collect an ingredient for the taco 
  - Garden Challenges 
    - Variable Challenge - Create an integer variable and increment it to “pick” tomatoes 
    - Operator Challenge – Operators, thoughts?? 
    - Loops and Lists Challenge - Create a loop to loop thru a collection of different types of toppings to collect them for the taco (tomatoes, lettuce, etc) 
  - Kitchen Challenges 
    - Multidimensional Array Challenge - Create a multidimensional array for topping and quantity 
    - Thread Challenge – Create a method to cook the beef. You will need to use thread.sleep to allow each pound of beef to be cooked to completion. Write a loop that loops thru the beef on hand and stirs the beef every 1 second until 5 seconds have been reached. 
    - Recursion Challenge – Now that you have successfully stocked the kitchen, lets build tacos. Create a method that recursively calls itself to build a taco until all ingredients have been used. 
  - Dining room 
    - App Challenge – Put everything together to build an app with methods that can successfully fill taco orders 
8. Help experience 
  - Get stuck on a problem 
9. Leader board/Achievements page with solutions, points and username 
10. Unit Test Validation with graphical animation results 
  - Unit test each challenge in the order in which they need to be completed. 
    - Graphic representation of error for the failed test to the users avatar 
      - Example: They didn’t chop the tomatoes so their avatar gets tomatoes thrown at them 
      - Example: The player forgot to put a taco shell on, the toppings fly all over the floor and player. 
11. Multi-user interaction/experience 
  - Ability to see other players avatar working on a challenge (avatar looped animation) 
  - Players can help other players with their challenges 
12. Three game play options: 
  - Single player working thru game 
  - Multiple players working thru game 
  - Competitive programming style event with Microsoft host and multiplayer. 
13. SOLITARE STYLE GAME WINNING TACO GRAPHICS!! 🌮🥳🃏 

 

## Achievements 

- “Beat the level” on every: 
  - Programming Level 
  - Language 
  - Scoring 
  - Fewer Lines Of Code 
  - Fewer Errors 
  - Best outcome 
  - Comments 
  - Well formatted 
  - Good variables names/Readability (some could be given by the host) 
- Multiple of the same “challenge” but with different aspects, trying to get this kind of feeling of collecting "them all"
