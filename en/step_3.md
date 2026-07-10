## Choose your colours

Change the quiz colour theme in `default.css` so that the page and result box match your chosen style.

From the **Project files** menu, select `default.css`.

Update the colour variables to choose a new look for your quiz.

You can copy this example or pick your own colours. You can use [this tool to choose colours](https://www.google.com/search?q=colour+picker){:target="_blank"}.

```css filename="default.css" line_numbers="true" line_number_start="1" line_highlights="6-12"
:root {
  /* Font variable */
  --font: 16px/1.25 'Raleway', sans-serif;
  
  /* Base Colours */
  --body-background: #F4F1DE; /* Set the page background colour. */
  --background: #2A9D8F; /* Set the colour of the header and question cards. */
  --header-font-colour: #ffffff; /* Set the text colour used in the header and result box. */
  --h1-colour: #264653; /* Set the dark highlight colour for headings and the result box background. */
  --h2-colour: #ffffff; /* Set the question text colour. */
  --button-background-colour: #E9C46A; /* Set the button background colour. */
  --button-font-colour: #264653; /* Set the button text colour. */
}
```

## Now run your code

Click on **Run**.

You should see the page colours update, and the text in the result box should show clearly when you check an answer.
