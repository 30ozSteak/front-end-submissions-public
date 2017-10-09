# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/davidbecker6081/PalettePicker)

#### Link to the Deployed Application
[heroku](https://david-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/davidbecker6081/PalettePicker/blob/add-comments-server/server.js)

## Completion

#### Were you able to complete the base functionality?

I've completed all of the base functionality although there were a few UI changes I wanted to make. Mostly to do with notifying the user of various actions such as creating a new project, displaying a project with no palettes, and creating a new palette.

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/davidbecker6081/PalettePicker/blob/master/public/js/scripts.js#L196-L214)

* Why were you proud of this piece of code?

I feel like this piece of code is a combination of so many things I've learned in the past 3 modules. It includes selecting jquery elements by parent container and then child. It includes a fetch call to an API endpoint that I built, consuming promises, a for in loop (which is pretty new to me), using bracket notation, and a little bit of functional javascript where one function is returning a value that another function then uses (running inside out).

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/davidbecker6081/PalettePicker/blob/master/public/js/scripts.js#L122-L141)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Most of the reason I feel sad about this code is because I think that there is great bit of refactoring to be done here. It actually is a pretty cool piece of code based on what it's doing, but it's doing wayyy too much for one function. This needs to be split out into multiple smaller functions and I need to find a way to get rid of the nested if/else statements. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://i.imgur.com/qE65GR6.png)

I have a few tests skipped because of this error, which I haven't figure out YET

[error](https://i.imgur.com/whpibuK.png)

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

It's been hard for me to understand all of the connection between database and the server.js file. But now at the end of the project, I feel like my grasp is on the incline. I made some choices that may not seem like efficient ones, completely for the sake of getting practice doing the things we're learning. For instance I chose to make a fetch call to get a specific palette to display on the main display when you clicked on it. This gave me the opportunity to do a couple of things again, one being making a fetch call to the API endpoint, two being writing another endpoint handler, and three being writing a test for this endpoint handler. It would have been a lot easier to store the color values in the DOM elements and just grab them straight from there, but I wanted the practice doing it the other way. 

[example of this](https://github.com/davidbecker6081/PalettePicker/blob/master/public/js/scripts.js#L196-L214)

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**x points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
