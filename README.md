# Snake-Game-Python

This repository contains a simple implementation of the classic Snake game using Pygame.

## Requirements

- Python 3.x
- Pygame

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/snake-game.git
   cd snake-game
   ```

2. Install the required dependencies:
   ```bash
   pip install pygame
   ```

## Running the Game

To run the game, execute the following command:
```bash
python main.py
```

## Gameplay Instructions

- Use the arrow keys to control the direction of the snake:
  - Up Arrow: Move Up
  - Down Arrow: Move Down
  - Left Arrow: Move Left
  - Right Arrow: Move Right

- The objective is to eat the apple. Each time the snake eats an apple, it grows in length.
- Avoid colliding with the walls or the snake's own body.

## Scoring

- Your score is displayed at the top right corner of the screen.
- The score is equivalent to the length of the snake.

## Game Over

- The game ends when the snake collides with itself.
- A game over screen will be displayed showing your final score.
- Press Enter to play again or Escape to exit the game.

## File Structure

- `main.py`: The main game logic and entry point for the game.
- `resources/`: Directory containing the images for the snake block and apple.

## Key Classes

### `Apple`

Represents the apple that the snake eats.

- `__init__(self, parent_screen)`: Initializes the apple.
- `draw(self)`: Draws the apple on the screen.
- `move(self)`: Randomly moves the apple to a new position on the screen.

### `Snake`

Represents the snake.

- `__init__(self, parent_screen, length)`: Initializes the snake with a given length.
- `draw(self)`: Draws the snake on the screen.
- `move_up(self)`, `move_down(self)`, `move_left(self)`, `move_right(self)`: Change the direction of the snake.
- `walk(self)`: Updates the snake's position based on the current direction.
- `increase_len(self)`: Increases the length of the snake.

### `Game`

Handles the game logic.

- `__init__(self)`: Initializes the game.
- `is_collision(self, x1, y1, x2, y2)`: Checks for collisions between the snake and the apple or itself.
- `play(self)`: Main game loop for handling game play.
- `display_score(self)`: Displays the current score.
- `show_game_over(self)`: Displays the game over screen.
- `reset(self)`: Resets the game state.
- `run(self)`: Main loop for handling events and running the game.

## License

This project is licensed under the MIT License.
