# Word Guessing Game 🎯

A simple Python word guessing game where players try to discover a hidden word by guessing one letter at a time before running out of attempts.

## Description

The program randomly selects a word from a predefined list and displays it as underscores (`_`). The player must guess letters to reveal the word.

- Correct guesses reveal matching letters.
- Incorrect guesses reduce the number of remaining attempts.
- The player wins by revealing the entire word before running out of attempts.

## Code

```python
import random

words = ["python", "coding", "computer", "programming"]
word = random.choice(words)

guessed = []
attempts = 6

while attempts > 0:
    display = ""

    for letter in word:
        if letter in guessed:
            display += letter
        else:
            display += "_"

    print(display)

    if "_" not in display:
        print("You win!")
        break

    guess = input("Guess a letter: ")

    if guess in word:
        guessed.append(guess)
    else:
        attempts -= 1
        print("Wrong! Attempts left:", attempts)
```

## How to Run

1. Install Python 3.
2. Save the code in a file named `word_guessing_game.py`.
3. Open a terminal or command prompt.
4. Run:

```bash
python word_guessing_game.py
```

## Example

```text
_______
Guess a letter: p

p______
Guess a letter: y

py____
Guess a letter: z
Wrong! Attempts left: 5
```

## Features

- Random word selection
- Interactive gameplay
- Tracks guessed letters
- Limited number of attempts
- Beginner-friendly Python project

## Concepts Used

- Python `random` module
- Lists
- Loops (`while`, `for`)
- Conditional statements (`if`, `else`)
- String manipulation
- User input handling

## Game Rules

1. A random word is selected.
2. The word is displayed as underscores.
3. Guess one letter at a time.
4. Correct letters are revealed.
5. Wrong guesses decrease your remaining attempts.
6. Win by revealing the entire word before attempts reach zero.

## Future Improvements

- Add more words and categories
- Display previously guessed letters
- Prevent duplicate guesses
- Add difficulty levels
- Show a "Game Over" message when attempts reach zero
- Create a graphical user interface (GUI)
- Implement a full Hangman drawing

## License

This project is open source and free to use.
