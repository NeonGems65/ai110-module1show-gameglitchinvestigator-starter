# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
Game's purpose is to guess a secret number after being guided with hints
- [ ] Detail which bugs you found.
Bug 1: Lower and higher indicators were not working
Bug 2: Start a new game feature was bugged and not letting the user submit new guesses towards a new game
- [ ] Explain what fixes you applied.

Switched the logic around for the higher and lower statements

Then made sure the state was changed whenever a user wanted to start
a new game

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. Launch the game with `python -m streamlit run app.py` and pick a difficulty in the sidebar (Easy, Normal, or Hard), which sets the number range and how many attempts you get.
2. Type a number into "Enter your guess" and click **Submit Guess 🚀**. The secret number now stays fixed across submits instead of changing every click.
3. Read the hint: if your guess is too high it correctly says "📉 Go LOWER!", and if it's too low it says "📈 Go HIGHER!" — the directions now match reality.
4. Keep guessing using the hints until you land on the secret number. You'll see "🎉 Correct!", balloons, and your final score before attempts run out.
5. Click **New Game 🔁** to start over — the game resets the secret, score, and status back to "playing" so you can immediately submit new guesses (no more "You already won" block).

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# ========================= X passed in 0.XXs =========================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
