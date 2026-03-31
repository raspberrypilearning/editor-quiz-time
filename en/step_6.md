<h2 class="c-project-heading--task">Keep score</h2>

### Step 1
Update `scripts.js` so correct answers add points and answered buttons can only be used once.

### Step 2
From the tab above the workspace, select **scripts.js**.

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 1
line_highlights: 2, 5, 15, 18-19
---
// Variables
var score = 0; // Store the player's score.

// Constants
const scoreText = document.querySelector("#scoreText"); // Find the score display in the header.

// Check answer function
function checkAnswer(question, result) {
  let answer = document.querySelector(`input[name="${question}"]:checked`);
  let qResult = document.querySelector(result);

  qResult.style.display = "block";

  if (answer) {
    document.querySelector("#" + question).disabled = true; // Stop the same button from scoring twice.
    if (answer.value === "correct") {
      qResult.innerText = "Correct";
      score += 1; // Add one point for a correct answer.
      scoreText.innerText = `Score: ${score}`; // Show the new score in the header.
    } else {
      qResult.innerText = "Incorrect";
    }
  } else {
    qResult.innerText = "Please select an answer";
  }
}
--- /code ---

</div>

<div class="c-project-output">
  <p>After a correct answer, the score increases by one and the same Check Answer button cannot be used again.</p>
</div>

### Step 3
**Test:** Click **Run**, answer a question correctly, and press **Check Answer**.

Your score should increase by one, and clicking the same button again should not add more points.
