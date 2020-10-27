# Tandem Excercise

# How to use

- Have the javascript files and the html file in the same folder/location. 
- Open the html file in a browser (I used Chrome only, may have overlooked compatibility issues with other browsers)
- click on answer 
- click the next button

---

## What the code does

Pulls 10 non-repeating questions (and answers) for a trivia quiz from json data and keeps track of correct answers to display at the end.

Clicking an answer reveals the correct answer by fading the incorrect answers and shows a "next" question button until the last question which will show the score and a button to "play again" by reloading the page.

---

## What the code does not

Store information (scores, users, etc), display score in real-time, load json from external source

---

## Ideas for upgrades

1. load json data from external source (otherwise it's hardcoded)
2. save scores for comparison later, locally or in a database
3. show scores real-time
4. accessibility upgrades (all point and click, but how does it look on a screen reader?, how does it work on a mobile platform?)
5. move javascript to separate file than the html (just for cleaning up, functionally shouldn't be too different)
6. clean up markup/css. a lot of inline styles and possibly incorrect use of bootstrap classes/markup
7. clean up javascript. probably a lot of inefficient use of jquery and javascript as well as difficult readability
8. any automated testing (currently none)
9. save which questions were answered to exclude them from subsequent run (if possible)
10. testing with other browsers for compatibility

---

## Troublesome tasks or things I learned as I went

1. json file could not be loaded locally (easily) because javascript doesn't have access to local files
2. json couldn't be loaded easily from external source because of CORS (tried github, maybe if everything was hosted on the same site but I was using by literally opening the html file in a browser, MAY be browser dependent but I user Chrome)
3. not all question answer arrays contained the same number of elements despite the instructions saying they would (resulting in out of bounds exceptions, maybe something that automated testing would catch?)
4. styling the answers to wrap when the text was too long while keeping it as large as possible
5. could not get the text to vertically align no matter the markup/classes used. gave up on it.
6. shuffling array so that answers weren't always in the same order
7. picking 10 random questions without duplication
8. removing events so that users couldn't continue to click the answers affecting internal counters
9. dynamically adding and removing elements (some exp with adding but been a while)
