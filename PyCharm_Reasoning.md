# Project: Random Number Guesser - Pseudocode

## 📋 Overview
This document outlines the logical flow and algorithmic structure for the Random Number Guessing Game. The goal of this pseudocode is to define input validation, random number generation, and the conditional game loop before implementation.

---

## 🛠️ Pseudocode Logic

```text
START

    # Initialize the random number generator
    IMPORT RANDOM

    # Phase 1: Range Definition & Input Validation
    WHILE TRUE
        PRINT "Enter lower bound:"
        INPUT user_input, save as 'lower'
        
        PRINT "Enter upper bound:"
        INPUT user_input, save as 'upper'
        
        # Check for logical range error
        IF upper is less than lower:
            PRINT "Error: Upper bound must be greater than lower bound. Please try again."
        ELSE:
            BREAK

    # Phase 2: Game Setup
    # Generate the target number within the specified criteria
    GET random number between 'lower' and 'upper', save as 'random_num'

    # Phase 3: The Main Game Loop
    WHILE TRUE
        PRINT "Guess the number:"
        INPUT user_input
        
        # Validation: Ensure guess is within the current bounds
        IF user_input is less than 'lower' OR user_input is greater than 'upper':
            PRINT "Invalid Input: Please guess a number within the limits established."
        
        # Condition: Correct Guess (Win State)
        ELIF user_input is equal to 'random_num':
            PRINT "Congratulations! You won! Thank you for playing."
            BREAK # Exit the game
            
        # Condition: Hint - Too High
        ELIF user_input is greater than 'random_num':
            PRINT "You guessed too high! Try Again!!"
            
        # Condition: Hint - Too Low
        ELIF user_input is less than 'random_num':
            PRINT "You guessed too low! Try Again!"

STOP

```

---

## 🧩 Logic Flow Breakdown

### 1. The Validation Loop

The first `WHILE TRUE` loop acts as a gatekeeper. It prevents the program from progressing if the user provides an impossible range (e.g., a lower bound of 10 and an upper bound of 5), ensuring the `random` function doesn't crash.

### 2. State Management

The program maintains the "State" of the game by comparing the `user_input` against the `random_num`.

* **Input < Target:** Provide low hint.
* **Input > Target:** Provide high hint.
* **Input == Target:** Trigger win sequence and terminate loop.

### 3. Boundary Enforcement

A specific `IF` statement is dedicated to ensuring the player stays within the range they defined, preventing "wasted" guesses outside the logic of the game.

---

### 🚀 Implementation Note

This pseudocode serves as the blueprint for the final Python script. By defining these conditions early, we ensure that edge cases (like guessing a number outside the range) are handled gracefully before the logic comparison occurs.
