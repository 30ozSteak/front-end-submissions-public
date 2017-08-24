# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/the-oem/jetfuel)

#### Link to the Deployed Application
[heroku](https://fuelthejets.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/the-oem/jetfuel/blob/commented-server/server.js)

## Completion

#### Were you able to complete the base functionality?
Yes, everything as I understand it in the base requirements is completed.

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?
I did not complete any of the extensions.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L56)

* Why were you proud of this piece of code?
_~ I wasn't sure what the best way to approach inline sorting of DOM elements would be, so getting this to work in a fairly simple manner felt good. Same could be said for the folder sorting code, as well._

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/the-oem/jetfuel/blob/master/public/assets/js/script.js#L195)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
_~ This is the code to toggle showing and hiding the list of links for a given folder. I did this using jQuery animate(), however I would like to have done something more slick using CSS and just use jQuery to add or remove appropriate classes to the DOM elements. It feels sluggish and choppy using the jQuery code. Sad Panda._

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![test suite](https://the-oem.github.io/assets/jetfuel-tests.png)

#### Please feel free to ask any other questions or make any other statements below!

* Anything else you wanna say! ~ _It felt pretty good to have the CircleCI tests running with each PR, and seeing the subsequent deploys to Heroku automatically was very cool :)_

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**18 points**: The application persists data in a SQL database but with correct relationships between folders and URLs, slight error with column fields re: uniqueness

* The [shortUrl](https://github.com/the-oem/jetfuel/blob/master/src/server/db/migrations/20170815155033_initial.js#L16) must be a unique value. If you generate two of the same short URLs, that point to different long URLs, one of them will be overridden. 

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**16 points**: The developer makes a series of small, atomic commits that document the evolution of their application though some are taking on a bit too much responsibility.

* Nice readme!
* Nice consistently formatted commit messages, though I'm concerned about the low number of commits. I'd expect a project like this to have a least 100; that's how granular and specific your changesets should be. Commits like [this](https://github.com/the-oem/jetfuel/commit/897d17af767053f44b6a66404050b81267bf3f62) are doing a bit too much and more than I'd expect given the commit message.
* Nice use of branches appropriately named
* I would avoid committing TO DO comments - file issues for those things instead or keep those on a branch, and remove them when the branch functionality is complete and you want to merge to master.
* [Ahhhhh](https://github.com/the-oem/jetfuel/blob/master/src/server/db/migrations/20170815155033_initial.js#L23)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
