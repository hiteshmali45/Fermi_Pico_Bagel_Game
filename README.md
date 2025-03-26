# Fermi Pico Bagel - Number Guessing Game

This project is a Python-based implementation of the classic "Fermi, Pico, Bagel" number guessing game. It guides players step-by-step to guess a secret number and provides feedback on the accuracy of their guesses.

## Game Rules
- *Fermi*: If a guessed digit is in the correct position.
- *Pico*: If a guessed digit exists in the secret number but is in the wrong position.
- *Bagel*: If neither the digit nor its position matches.

Play the game online to understand the basic concept: [Game Link](https://communicrossings.com/html/js/pfb.htm)

## Features
- Accepts user input for the guessed number.
- Validates input to ensure it matches the length of the secret number and doesn't contain duplicate digits.
- Provides feedback after each guess based on the game's rules.
- Allows repeated guessing until the correct number is guessed.

## How It Works
The implementation follows a step-by-step approach:
1. *Original Number Setup:* Define the secret number (original_number) in string format.
2. *User Input:* Prompt the player to enter their guess (guess_number).
3. *Validation:*
   - Ensure that the guess has the correct number of digits.
   - Check for any duplicate digits in the guessed number.
4. *Feedback Mechanism:*
   - Append feedback ("Fermi", "Pico", or "Bagel") to an output list based on the guessing rules.
   - Display the feedback as a single output string.
5. *Winning Condition:* If the player correctly guesses all digits and positions, they win the game!
6. *Loop:* Continue until the correct number is guessed, using continue and break statements where appropriate.

## Code Overview
The notebook contains:
- Step-by-step instructions with accompanying Python code.
- Key sections including validation, digit checks, feedback generation, and winning condition handling.

## Example Usage
python
original_number = '123'

while True:
    guess_number = input("Enter a number: ")

    if len(original_number) != len(guess_number):
        print("Invalid input! Number must have the correct number of digits.")
        continue

    if len(set(guess_number)) != len(guess_number):
        print("Duplicate number detected! Please try again.")
        continue

    output = []
    for i in range(len(guess_number)):
        if guess_number[i] == original_number[i]:
            output.append("Fermi")
        elif guess_number[i] in original_number:
            output.append("Pico")

    if not output:
        print("Bagels")
    else:
        print(" ".join(output))

    if output == ["Fermi"] * len(original_number):
        print("You win!")
        break
    else:
        print("Try again!")


## Installation
1. Clone this repository:
   bash
   git clone https://github.com/hiteshmali45/Fermi_Pico_Bagel_Game
   
2. Open the Jupyter Notebook and follow the step-by-step instructions.
