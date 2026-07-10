## Show one question at a time

Hide every question card by default, then use JavaScript to show only the first one when the page loads.

You will need to edit both the `style.css` and the `scripts.js` files so that the CSS **hides** all the question cards, and the JavaScript **brings back** the first one.

## Step 1

From the **Project files** menu, select `style.css`.

Add the following lines to hide all the question cards:

```css filename="style.css" line_numbers="true" line_number_start="34" line_highlights="41-42"
.q-container {
  background-color: var(--background);
  width: 90%;
  max-width: 600px;
  margin: 100px auto 0;
  border-radius: 10px;
  padding: 30px;
  display: none; /* Hide every question until JavaScript shows one. */
  opacity: 0; /* Start hidden so animations can fade questions in. */
}
```

## Step 2

From the tabs above the workspace, select `scripts.js` so that you can update the JavaScript next.

Add the following code to show the first card:

```javascript filename="scripts.js" line_numbers="true" line_number_start="4" line_highlights="6,30-31"
// Constants
const scoreText = document.querySelector("#scoreText");
const questions = document.querySelectorAll(".q-container"); // Collect all of the question cards.

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
    } else {
      qResult.innerText = "Incorrect";
    }
  } else {
    qResult.innerText = "Please select an answer";
  }
}

// Display first question
questions[0].style.display = "block"; // Show the first card as soon as the page loads.
questions[0].style.opacity = 1; // Make sure the first card is fully visible.
```

## Now run your code

Click on **Run**.

Check that only the first question shows when the page opens.
