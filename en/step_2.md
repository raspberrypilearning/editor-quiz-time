## Check the answer

Create a `checkAnswer` function in `scripts.js` so that the quiz can show whether an answer is correct.

From the **Project files** menu, select `scripts.js`.

Add the following code:

```javascript filename="scripts.js" line_numbers="true" line_number_start="7" line_highlights="8-23"
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
```

## Now run your code

Click on **Run**, choose an answer, and press **Check Answer**.

The result box should appear and show **"Correct"**, **"Incorrect"**, or **"Please select an answer"**.
