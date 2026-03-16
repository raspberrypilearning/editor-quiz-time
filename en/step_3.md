<h2 class="c-project-heading--task">Check the answer</h2>

--- task ---
Create a `checkAnswer` function in `scripts.js` so the quiz can show whether an answer is correct.
--- /task ---

Line numbers are best-effort in this rewritten project.

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 7
line_highlights: 8-20
---
// Check answer function
function checkAnswer(question, result) {
  let answer = document.querySelector(`input[name="${question}"]:checked`); // Find the selected answer for this question.
  let qResult = document.querySelector(result); // Find the result box for this question.

  qResult.style.display = "block"; // Show the hidden result box.

  if (answer) { // Only check the answer if the user selected one.
    if (answer.value === "correct") {
      qResult.innerText = "Correct"; // Show a success message for the right answer.
    } else {
      qResult.innerText = "Incorrect"; // Show a different message for a wrong answer.
    }
  } else {
    qResult.innerText = "Please select an answer"; // Prompt the user if nothing was selected.
  }
}
--- /code ---

</div>

<div class="c-project-output">
<pre>The result box appears underneath the answers and shows Correct, Incorrect, or Please select an answer.</pre>
</div>

--- task ---
**Test:** Click **Run**, choose an answer, and press **Check Answer**.

The result box should appear and show **Correct**, **Incorrect**, or **Please select an answer**.
--- /task ---
