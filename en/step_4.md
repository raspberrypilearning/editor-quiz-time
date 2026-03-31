<h2 class="c-project-heading--task">Add more questions</h2>

### Step 1
Copy and paste the question container two times, and edit them so your quiz has three questions that use unique names, ids, and result boxes.

### Step 2
From the tab above the workspace, select **index.html**.

Paste the new question containers underneath the first question container, before the closing `</main>` tag.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 30
line_highlights: 31-59
---
      </div>
      <div class="q-container">
        <h1>Question 2</h1> <!-- Update the number for the second question. -->
        <h2>Which bird is known for its ability to copy human speech?</h2> <!-- Write a new question here. -->

        <input type="radio" name="q2" value="" id="q2a1">
        <label for="q2a1">Sparrow</label><br>
        <input type="radio" name="q2" value="" id="q2a2">
        <label for="q2a2">Pigeon</label><br>
        <input type="radio" name="q2" value="correct" id="q2a3">
        <label for="q2a3">Parrot</label><br> <!-- Give the correct answer value="correct". -->

        <div class="result" id="result2"></div> <!-- Match the result box to question 2. -->
        <button id="q2" onclick="checkAnswer('q2', '#result2')">Check Answer</button> <!-- Pass q2 into the function. -->
      </div>

      <div class="q-container">
        <h1>Question 3</h1> <!-- Repeat the same pattern for question 3. -->
        <h2>Which animal is known for its distinctive black and white stripes?</h2>

        <input type="radio" name="q3" value="" id="q3a1">
        <label for="q3a1">Hippopotamus</label><br>
        <input type="radio" name="q3" value="" id="q3a2">
        <label for="q3a2">Giraffe</label><br>
        <input type="radio" name="q3" value="correct" id="q3a3">
        <label for="q3a3">Zebra</label><br>

        <div class="result" id="result3"></div> <!-- Use a new result id for the third question. -->
        <button id="q3" onclick="checkAnswer('q3', '#result3')">Check Answer</button> <!-- Pass q3 into the function. -->
      </div>
    </main>
--- /code ---

</div>

<div class="c-project-output">
  <p>The page now shows three separate question cards, each with its own answers, result box, and Check Answer button.</p>
</div>

### Step 3
**Test:** Click **Run**.

You should see three question cards on the page, and each card should have its own **Check Answer** button.
