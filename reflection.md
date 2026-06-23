# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
It seemed like a guessing game of numbers 
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
The hints were innacurate, it told me to go lower when the number was actually higher
Also told me to go higher when the number was actually lower

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| 1   |  correct or go higher  |   go lower              
 99   |   correct or go lower  |    go higher
 one wrong answer | score of 65 | score of 55
 start a new game | starts a new game and refreshes everything | You already won

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
Claude
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
The AI Suggestion that told me that status was still set to won after 
starting a new game. I verfied this by going through the code myself and 
seeing where the AI quoted its work
- Give one example of an AI suggestion that was incorrect or misleading 
(including what the AI suggested and how you verified the result).
None

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  Ran a test to see if the game would start normally, and it showed that 
  the edit AI made to my code was successful
- Did AI help you design or understand any tests? How?
Yes, it helped me understand the syntax behind it and what it 
was trying to test for

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Basically, every button or interaction with Streamlit causes the script to run
again

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
Using Pytests and manually checking AI Code
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
Stop it before it keeps hallucinating further
- In one or two sentences, describe how this project changed the way you think about AI generated code.
Taught me that AI is very good at generating substance, but not good at 
checking its own work. You have to force it via tests or tell it directl
when something is wrong. 
