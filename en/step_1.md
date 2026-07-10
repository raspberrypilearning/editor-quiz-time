## Create your first question

Click on **Run** so that you can see the starter project before you change it.

You should see a placeholder quiz title and one question card, and no **Check Answer** button yet.

From the **Project files** menu, select `index.html`.

```html filename="index.html" line_numbers="true" line_number_start="8" line_highlights="8,12,17,20,23,26,28-29"
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
```

## Now run your code

Click on **Run**.

You should now see your quiz title, one question, three answers, and a **Check Answer** button.
