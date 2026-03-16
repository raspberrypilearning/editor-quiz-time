<h2 class="c-project-heading--task">Show the next question</h2>

--- task ---
Track which question is active and move to the next card after each checked answer.
--- /task ---

--- task ---
From the file menu, select **scripts.js**.
--- /task ---

--- task ---

Add the `NextQ` function to move to the next question when the user answers:

--- /task ---

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 1
line_highlights: 3,22,25,36-47
---
// Variables
var score = 0;
var currentQ = 0; // Keep track of the current question index.

// Constants
const scoreText = document.querySelector("#scoreText");
const questions = document.querySelectorAll(".q-container");

// Check answer function
function checkAnswer(question, result) {
  let answer = document.querySelector(`input[name="${question}"]:checked`);
  let qResult = document.querySelector(result);

  qResult.style.display = "block";

  if (answer) {
    document.querySelector("#" + question).disabled = true;
    if (answer.value === "correct") {
      qResult.innerText = "Correct";
      score += 1;
      scoreText.innerText = `Score: ${score}`;
      nextQ(); // Move on after a correct answer.
    } else {
      qResult.innerText = "Incorrect";
      nextQ(); // Move on after an incorrect answer too.
    }
  } else {
    qResult.innerText = "Please select an answer";
  }
}

// Display first question
questions[0].style.display = "block";
questions[0].style.opacity = 1;

// Next question function
function nextQ() {
  questions[currentQ].classList.add("fade-out"); // Animate the current card out.
  setTimeout(() => {
    if (currentQ < questions.length - 1) {
      questions[currentQ].style.display = "none"; // Hide the current card after the delay.
      currentQ++; // Move to the next question in the list.
      questions[currentQ].classList.add("slide-left"); // Animate the next card in.
      questions[currentQ].style.display = "block"; // Show the next question.
    }
  }, "2000");
}
--- /code ---

</div>

<div class="c-project-output">
  <p>After you answer a question, the current card fades out and the next question slides into view.</p>
</div>

--- task ---
**Test:** Click **Run** and answer the first question.

The current question should fade away and the next question should appear after a short delay.
--- /task ---
