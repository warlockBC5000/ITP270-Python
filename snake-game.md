# Snake Game

In this tutorial, you will create a Snake Game using a graphical library.

Below is a basic example of creating a simple Snake game using Pygame. 

## Make sure you have Pygame installed before running this code.

```pip3 install pygame```

## Steps:

Step 1: Import Libraries

Import the necessary libraries, including pygame for creating the game.<br>

Step 2: Initialize Pygame

Initialize Pygame to set up the game environment.<br>

Step 3: Define Constants

Set constants for the game, including screen width and height, grid size, colors, and directions.<br>

Step 4: Initialize the Screen

Create the game screen with a specified width and height.
Set the window caption.<br>

Step 5: Set Up Initial Game State

Initialize the snake's initial position and direction.
Initialize the food's initial position.
Set the initial score to 0.
Initialize the game over flag to False.<br>

Step 6: Main Game Loop

Start the main game loop, which runs until the game over flag becomes True.<br>

Step 7: Event Handling

Handle events such as quitting the game or changing the snake's direction based on user input.<br>

Step 8: Move the Snake

Calculate the new head position for the snake based on its current position and direction.<br>

Step 9: Collision Detection

Check for collisions:
If the snake collides with the food:
Increase the score.
Generate new food at a random position.
If the snake collides with itself or goes out of bounds:
Set the game over flag to True.<br>

Step 10: Update the Display

Clear the screen.
Draw the food.
Draw the snake segments.
Update the display to show the current game state.<br>

Step 11: Frame Rate Control

Cap the frame rate to control the speed of the game.<br>

Step 12: Game Over

When the game ends, display a "Game Over" message along with the player's score.
Wait for a key press to exit the game.<br>

Step 13: Quit Pygame

Quit Pygame when the game is done.


## Snake Game Code

```python
import pygame
import random

# Initialize Pygame
pygame.init()

# Constants
WIDTH, HEIGHT = 640, 480
GRID_SIZE = 20
GRID_WIDTH = WIDTH // GRID_SIZE
GRID_HEIGHT = HEIGHT // GRID_SIZE

# Colors
WHITE = (255, 255, 255)
GREEN = (0, 255, 0)
RED = (255, 0, 0)

# Directions
UP = (0, -1)
DOWN = (0, 1)
LEFT = (-1, 0)
RIGHT = (1, 0)

# Initialize the screen
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Snake Game")

# Snake initial position and direction
snake = [(GRID_WIDTH // 2, GRID_HEIGHT // 2)]
snake_direction = RIGHT

# Food initial position
food = (random.randint(0, GRID_WIDTH - 1), random.randint(0, GRID_HEIGHT - 1))

# Score
score = 0

# Game over flag
game_over = False

# Main game loop
clock = pygame.time.Clock()
while not game_over:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            game_over = True
        elif event.type == pygame.KEYDOWN:
            if event.key == pygame.K_UP and snake_direction != DOWN:
                snake_direction = UP
            elif event.key == pygame.K_DOWN and snake_direction != UP:
                snake_direction = DOWN
            elif event.key == pygame.K_LEFT and snake_direction != RIGHT:
                snake_direction = LEFT
            elif event.key == pygame.K_RIGHT and snake_direction != LEFT:
                snake_direction = RIGHT

    # Move the snake
    new_head = (snake[0][0] + snake_direction[0], snake[0][1] + snake_direction[1])

    # Check for collisions
    if new_head == food:
        snake.insert(0, food)
        score += 1
        food = (random.randint(0, GRID_WIDTH - 1), random.randint(0, GRID_HEIGHT - 1))
    elif (
        new_head in snake
        or new_head[0] < 0
        or new_head[0] >= GRID_WIDTH
        or new_head[1] < 0
        or new_head[1] >= GRID_HEIGHT
    ):
        game_over = True
    else:
        snake.insert(0, new_head)
        snake.pop()

    # Clear the screen
    screen.fill(WHITE)

    # Draw the food
    pygame.draw.rect(
        screen, GREEN, (food[0] * GRID_SIZE, food[1] * GRID_SIZE, GRID_SIZE, GRID_SIZE)
    )

    # Draw the snake
    for segment in snake:
        pygame.draw.rect(
            screen,
            RED,
            (segment[0] * GRID_SIZE, segment[1] * GRID_SIZE, GRID_SIZE, GRID_SIZE),
        )

    # Update the display
    pygame.display.update()

    # Cap the frame rate
    clock.tick(10)

# Game over screen
font = pygame.font.Font(None, 36)
game_over_text = font.render("Game Over", True, (255, 0, 0))
score_text = font.render(f"Score: {score}", True, (0, 0, 0))
screen.blit(game_over_text, (WIDTH // 2 - 100, HEIGHT // 2 - 50))
screen.blit(score_text, (WIDTH // 2 - 50, HEIGHT // 2))
pygame.display.update()

# Wait for a key press to exit
waiting_for_key = True
while waiting_for_key:
    for event in pygame.event.get():
        if event.type == pygame.KEYDOWN:
            waiting_for_key = False

pygame.quit()
```

