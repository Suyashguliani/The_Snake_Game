Description of the Code: 
Snake Game Implementation
This Python program implements the classic Snake Game using the turtle module. The game involves controlling a snake to eat food while avoiding collisions with the walls or itself. Here's a detailed description of the code and its components:

Code Overview
Imports:

time: Used to control the speed of the game loop.
turtle.Screen: Sets up the game screen for graphical interaction.
Custom Modules:
Snake: Handles snake creation, movement, and growth.
Food: Manages the placement of food on the screen.
Scoreboard: Keeps track of the player's score and displays the game-over message.
Screen Setup:

Creates a 600x600 black game screen with the title "My Snake Game."
Turns off automatic screen updates using screen.tracer(0) for smoother animations.
Object Initialization:

snake: An instance of the Snake class, representing the snake.
food: An instance of the Food class, representing the food the snake eats.
scoreboard: An instance of the Scoreboard class, managing the score and displaying game messages.
Controls:

screen.listen(): Listens for user input.
Arrow keys (Up, Down, Left, Right) are mapped to methods for changing the snake's direction.
Game Loop
The main game loop (while game_is_on) handles the gameplay:

Screen Update:

The game screen updates with screen.update() after each iteration.
Snake Movement:

The snake moves continuously, controlled by the snake.move() method.
Food Collision:

If the snake's head is within a distance of 15 units from the food, the food is "eaten":
food.refresh(): Places the food in a new random location.
snake.extend(): Adds a segment to the snake's body.
scoreboard.increase_score(): Updates the player's score.
Wall Collision:

If the snake's head crosses the screen boundaries, the game ends, and the scoreboard displays a "Game Over" message.
Self-Collision:

If the snake's head collides with any other segment of its body, the game ends.
Game Over and Exit
Displays "Game Over" using the scoreboard.game_over() method when the game ends.
The game window remains open until the user clicks it (screen.exitonclick()).
