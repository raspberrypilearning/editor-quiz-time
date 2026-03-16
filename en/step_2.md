<h2 class="c-project-heading--task">Create your first question</h2>

--- task ---
Change the quiz title and build the first multiple-choice question in `index.html`.
--- /task ---

Line numbers are best-effort in this rewritten project.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 8
line_highlights: 8,12,17,20,23,26,28-29
---
    <title>Wildlife quiz</title> <!-- Change this to match your quiz topic. -->
  </head>
  <body>
    <header class="header">
      <span class="sitename">Wildlife quiz</span> <!-- Show the same title in the page header. -->
    </header>
    <main>
      <div class="q-container">
        <h1>Question 1</h1>
        <h2>What is the largest living cat species?</h2> <!-- Write your first question here. -->

        <input type="radio" name="q1" value="correct" id="q1a1">
        <label for="q1a1">Tiger</label><br> <!-- Keep the correct answer marked with value="correct". -->

        <input type="radio" name="q1" value="" id="q1a2">
        <label for="q1a2">Cheetah</label><br> <!-- Use a blank value for an incorrect answer. -->

        <input type="radio" name="q1" value="" id="q1a3">
        <label for="q1a3">Lion</label><br> <!-- Give each answer its own id. -->

        <div class="result" id="result1"></div> <!-- JavaScript will show the result text here. -->
        <button id="q1" onclick="checkAnswer('q1', '#result1')">Check Answer</button> <!-- This button will check question 1. -->
      </div>
--- /code ---

</div>

<div class="c-project-output">
<pre>Your page shows the quiz title, one question card, three answer options, and a Check Answer button.</pre>
</div>

--- task ---
**Test:** Click **Run**.

You should see your quiz title, one question, three answers, and a **Check Answer** button.
--- /task ---
