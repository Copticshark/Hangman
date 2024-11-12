# Hangman

A terminal-based Hangman game implementation in C++ that supports both single-player and multiplayer modes.

## Features

- **Single Player Mode**: Play against the computer with randomly selected words from different categories
- **Multiplayer Mode**: Play with friends, taking turns to set words and guess
- **Multiple Categories**:
  - Animals
  - Kitchen/Foods
  - Random Objects
  - Custom words (in multiplayer mode)
- **Visual Hangman Display**: ASCII art representation of the hangman
- **Input Validation**: Prevents duplicate guesses and ensures single-letter inputs

## Prerequisites

- C++ compiler (g++ recommended)
- Standard C++ libraries

## Installation

1. Clone the repository:
```bash
git clone [your-repository-url]
cd hangman-game
```

2. Create the required text files:
```bash
mkdir textFiles
touch textFiles/Animals.txt
touch textFiles/Foods.txt
touch textFiles/RandomObjects.txt
```

3. Add words to the text files (one word per line)

4. Compile the game:
```bash
g++ run.cpp Game.cpp Board.cpp -o hangman
```

## Usage

1. Run the game:
```bash
./hangman
```

2. Choose game mode:
   - Press 'S' for Single Player
   - Press 'M' for Multiplayer

3. For multiplayer mode, enter the number of players

### Game Rules

- Each player gets 6 attempts to guess the word
- In multiplayer mode, players take turns setting words for others to guess
- Spaces in words are represented by '-'
- Incorrect guesses result in the hangman being drawn piece by piece
- The game ends when either:
  - The word is correctly guessed
  - The hangman drawing is completed (6 incorrect guesses)

## Project Structure

- `run.cpp`: Main game entry point
- `Game.cpp/hpp`: Game logic and mechanics
- `Board.cpp/hpp`: Hangman board display and state management
- `textFiles/`: Directory containing word lists for single-player mode
  - `Animals.txt`: List of animal words
  - `Foods.txt`: List of food-related words
  - `RandomObjects.txt`: List of miscellaneous words
