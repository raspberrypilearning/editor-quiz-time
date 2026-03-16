<h2 class="c-project-heading--task">Finish the quiz</h2>

--- task ---
Add a full-marks message and a retry link, then update the last question so the quiz shows a final result instead of another card.
--- /task ---

--- task ---
From the file menu, select **index.html**.
--- /task ---

--- task ---

Add a special message if the player scores full marks:

--- /task ---

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 61
line_highlights: 65-66
---
        <input type="radio" name="q3" value="correct" id="q3a3">
        <label for="q3a3">Zebra</label><br>

        <div class="result" id="result3"></div>
        <div class="fullMarks">Well done! All correct!</div> <!-- Show this message for a perfect score. -->
        <a class="retry" href="index.html">Have another go!</a> <!-- Show this link if the player wants to retry. -->
        <button id="q3" onclick="checkAnswer('q3', '#result3')">Check Answer</button>
      </div>
--- /code ---

</div>


--- task ---
From the file menu, select **scripts.js**.
--- /task ---

--- task ---

Show the player their final score and let the player try again:

--- /task ---

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 5
line_highlights: 8-9,44-50,56-57
---
// Constants
const scoreText = document.querySelector("#scoreText");
const questions = document.querySelectorAll(".q-container");
const fullMarks = document.querySelector(".fullMarks"); // Find the perfect-score message.
const retry = document.querySelector(".retry"); // Find the retry link.

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
      nextQ();
    } else {
      qResult.innerText = "Incorrect";
      nextQ();
    }
  } else {
    qResult.innerText = "Please select an answer";
  }
}

// Next question function
function nextQ() {
  questions[currentQ].classList.add("fade-out");
  setTimeout(() => {
    if (currentQ < questions.length - 1) {
      questions[currentQ].style.display = "none";
      currentQ++;
      questions[currentQ].classList.add("slide-left");
      questions[currentQ].style.display = "block";
    } else {
      scoreText.innerText = `Final score: ${score}/${questions.length}`; // Replace the running score with the final total.
      scoreText.classList.add("glowing"); // Make the final score stand out.
      if (score === questions.length) {
        fullMarks.style.display = "block"; // Reveal the congratulations message.
      } else {
        retry.style.display = "block"; // Let the player try again.
      }
    }
  }, "2000");
}

// Display first question
questions[0].style.display = "block";
questions[0].style.opacity = 1;
--- /code ---

</div>

<div class="c-project-output">
  <p>The quiz ends with a glowing final score, followed by either a full-marks message or a retry link.</p>
</div>

--- task ---
**Test:** Click **Run** and finish the quiz.

You should see a glowing final score, then either a full-marks message or a retry link.
--- /task ---
