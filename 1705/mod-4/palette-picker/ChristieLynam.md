# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/christielynam/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-cl.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/christielynam/palette-picker/blob/server-comments/server.js)


## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

Yes, with the exception of 1 minor bug. When i click the delete icon, I originally get a 500 error (/api/v1/palettes/undefined). When I refresh the page and click it again, it removes the palette from the database correctly.

#### Which extensions, if any, did you complete?

Ability to modify color in the generator

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L20-L32)

* Why were you proud of this piece of code?

I was proud of making a nested fetch call for each project to append that projects palettes on page load. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L44-L59)
[more sad code](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L102-L116)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I feel like I should probably be able to write both append palette functions with one function, but have just not had the time to do a major refactor.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="763" alt="screen shot 2017-10-06 at 10 54 46 pm" src="https://user-images.githubusercontent.com/20754511/31304860-7f119a20-aae9-11e7-841a-32b3c3b3ae24.png">

#### Please feel free to ask any other questions or make any other statements below!

-----


# Instructor Feedback (Brittany)

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

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Some instances of [commented](https://github.com/christielynam/palette-picker/commit/c64452e04203af1078e10c2ba9e10a9a748cf081#diff-78c12f5adc1848d13b1c6f07055d996eR5). [out](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cR51). [code](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cL54) and [console.logs](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cR63) You can use `git stash` to hide changes that you don't want to commit yet and pop them back on when you want them back with `git stash pop`. 

* Nice, consistent formatting of your commit messages but I'd recommend capitalizing the first letter of each commit message. This makes them even more consistent with the auto-generated Merge Commits, and is the most common practice on development teams.

* Good use of branches, pull requests are kind of irrelevant in this scenario because you are working individually and don't have anyone reviewing your code. You can use the typical merge or rebase workflow for getting your changes into master when you're working solo. This keeps your history clean and free of excessive merge commits, without having to push changes directly to master.

* This [commit](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cR63) probably does a little too much - if the problem was that you forgot a leading slash in your api endpoint, that should be the only single-line change in this commit. Front-end changesets are irrelevant and should be put into a subsequent commit, or the commit message should reflect that all of these changes are being made.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
