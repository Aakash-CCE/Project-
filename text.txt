Python project where the user guesses a randomly generated integer within a specified range. This can be a great beginner project to practice conditionals, loops, and user input.

---

### 🎯 **Number Guessing Game in Python**

```python
import random

def number_guessing_game():
    print("🎲 Welcome to the Number Guessing Game!")
    lower = int(input("Enter the lower bound: "))
    upper = int(input("Enter the upper bound: "))

    if lower >= upper:
        print("Invalid range. The upper bound must be greater than the lower bound.")
        return

    number_to_guess = random.randint(lower, upper)
    attempts = 0

    while True:
        guess = input(f"Guess a number between {lower} and {upper}: ")

        # Validate input
        if not guess.isdigit():
            print("Please enter a valid number.")
            continue

        guess = int(guess)
        attempts += 1

        if guess < number_to_guess:
            print("Too low! Try again.")
        elif guess > number_to_guess:
            print("Too high! Try again.")
        else:
            print(f"🎉 Correct! You guessed it in {attempts} attempts.")
            break

# Run the game
number_guessing_game()
```

---

### ✅ Features

* User-defined range
* Input validation
* Feedback on each guess
* Tracks number of attempts

---

### 🔁 Optional Enhancements

* Limit number of attempts
* Add a play-again option
* Include difficulty levels
* Use GUI with `tkinter`

Let me know if you'd like a version with enhancements or a graphical interface!