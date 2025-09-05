## How to Run
```bash
ruby game.rb

## README.FILE -- 
Here’s a complete README.md for this`Greedy_Game_onboarding` project, summarizing the game, file structure, setup, running instructions, and testing guide.

# 🎲 Greedy Game Onboarding

A simple Ruby implementation of the dice game **Greed**, with an interactive CLI and RSpec test suite.

---

## 📜 Table of Contents
1. [Overview](#overview)
2. [Game Rules](#game-rules)
3. [Project Structure](#project-structure)
4. [Setup & Installation](#setup--installation)
5. [Running the Game](#running-the-game)
6. [Running the Test Suite](#running-the-test-suite)
7. [File-by-File Explanation](#file-by-file-explanation)

---

## Overview
Greedy Game is a turn-based dice game where players roll dice to score points. The first player to reach the end game score triggers the final round. The highest score at the end wins.

This project is built in pure Ruby and comes with an RSpec test suite for verification.

---

## Game Rules
- Each turn, you roll up to 5 dice.
- Certain combinations score points:
  - Triple 1s = 1000 points
  - Triple (2–6) = face value × 100 points
  - Single 1 = 100 points
  - Single 5 = 50 points
- To enter the game, a player must score at least 300 points in a single turn.
- First to 3000 points triggers the final round.
- In the final round, each remaining player gets one more turn.
- The player with the highest score wins.

---

## Project Structure

Greedy_Game_onboarding--
│
├── dice_set.rb        # Handles rolling n dice and storing the result
├── game.rb            # Main game logic and flow
├── greed_score.rb     # Scoring rules for dice rolls
├── player.rb          # Player data structure
├── Gemfile            # Ruby dependencies
├── Gemfile.lock       # Dependency lock file
├── .rspec             # RSpec config to load spec\_helper
├── spec/
│   ├── spec_helper.rb       # RSpec global configuration
│   ├── dice_set_spec.rb     # Tests for DiceSet class
│   ├── greed_score_spec.rb  # Tests for scoring logic
│   ├── player_spec.rb       # Tests for Player class
│   └── game_spec.rb         # Tests for Game class

---

## Setup & Installation for this project-

### 1. Install Ruby
Make sure you have Ruby **2.6.6** or higher installed.  
If you use `rbenv`:

rbenv install 2.6.6
rbenv local 2.6.6

Check version:

ruby -v


### 2. Install Bundler

gem install bundler


---

### 3. Install Dependencies


bundle install


If RSpec is not yet in your Gemfile:

bundle add rspec
rspec --init


---

## Running the Game

From the project root:


ruby game.rb

Follow on-screen prompts to:

* Enter the number of players
* Play turns
* Decide whether to roll again or keep your score

---

## Running the Test Suite

### 1. Ensure RSpec is installed


bundle add rspec
rspec --init


### 2. Save Spec Files

The provided test files are inside the `spec/` folder:

* `spec/dice_set_spec.rb`
* `spec/greed_score_spec.rb`
* `spec/player_spec.rb`
* `spec/game_spec.rb`

### 3. To Run All Tests


rspec

✅ **If everything passes, we can see all green output.**

---

## File-by-File Explanation

### **dice_set.rb**

* Class: `DiceSet`
* Handles rolling a given number of dice.
* `roll(n)` → Returns an array of `n` integers between 1 and 6.
* Stores the last roll in `@values`.

### **game.rb**

* Class: `Game`
* Coordinates the entire game:

  * Sets up players
  * Loops through turns
  * Tracks total scores
  * Triggers the final round
  * Declares the winner

### **greed_score.rb**

* Method: `score(dice)`
* Implements scoring rules:

  * Triples, singles for 1s and 5s
  * Returns `[points, scoring_dice_array]`

### **player.rb**

* Class: `Player`
* Stores:

  * Player name
  * Total score
  * Whether they’ve entered the game (`in_game` flag)

### **Gemfile / Gemfile.lock**

* Manage Ruby dependencies.
* Add gems like `rspec` for testing.

### **.rspec**

* Ensures RSpec always loads `spec_helper.rb`.

### **spec/spec_helper.rb**

* Base configuration for all specs.

### **spec/dice_set_spec.rb**

* Tests for dice rolling behavior and `@values` tracking.

### **spec/greed_score_spec.rb**

* Tests scoring logic for various dice combinations.

### **spec/player_spec.rb**

* Tests initialization, getters, and setters for Player.

### **spec/game_spec.rb**

* Tests core game logic (player setup, scoring entry, roll again prompt).
* Uses `allow(...).to receive(:gets)` to simulate user input.

// Successfully Build the Greed game assignment.
---
