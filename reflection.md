# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?it asked for a number to be guessed and gave hints to guess correctly 
- List at least two concrete bugs you noticed at the start: the hints were backwards; when clicking a new game after guessing the correct number, the game doesn't reset, attempts counter is off
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| 11    | go higher hint      go lower hint    none
| 5     | go higher hint      go lower hint     none
| 2     | go higher hint      go lower hint     none

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)? i use chatGPT/claude
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result). 
      - I used AI to fix the new game logic, so that game resets to a new game when the button is clicked. Ai suggested   st.session_state.score = 0
    st.session_state.status = "playing"
    st.session_state.history = []. I verified it by playing a game till I got it correct, and clicked New Game. 
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
I didn't the AI enough to see if it was measleading. 

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?  I ran the game to test those bugs
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code. 
  def test_winning_guess():
    # If the secret is 50 and guess is 50, it should be a win
    outcome, message = check_guess(50, 50)
    assert outcome == "Win"  
    The test passed. 
- Did AI help you design or understand any tests? How? AI updated the test. 

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
