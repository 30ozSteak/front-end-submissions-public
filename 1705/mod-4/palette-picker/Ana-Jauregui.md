# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[Ana Jauregui palette-picker](https://github.com/anajauregui/Palette-Pickr)

#### Link to the Deployed Application
[Ana Jauregui heroku app](https://palette-pickr.herokuapp.com/)

#### Link to your annotated server file
[Ana Jauregui server file with comments](https://github.com/anajauregui/Palette-Pickr/blob/serverJS-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to complete the base functionality requirements! 

#### Which extensions, if any, did you complete?

I was not able to complete any extensions, I would like to complete functionality for proper deletion of entire projects. I am mostly there but I need to add an acurate icon that serves as a visual to the user and I need to appropriately link the event handler so that I avoid removing parts from the DOM. 

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
happy code:  

<img width="648" alt="screenshot 2017-10-08 23 21 48" src="https://user-images.githubusercontent.com/20731901/31325908-8f4546e8-ac7f-11e7-95f7-696f52282124.png">

* Why were you proud of this piece of code?

- Lines 177 to 200 of scripts.js file. Although it does seem like a function that could use some refactoring, it took me quite some time to get to this resolution, and I was proud of the new approach that I finally decided upon using $.makeArray(). I had several bugs to work through in the solution of updating the large palette generator view with a selection from the saved list. Initially I did not think this would take me as long as it did, and therefore I am proud of the result from the struggle.

#### Link to a specific block of your code on GitHub that you feel not great about
sad code: 

<img width="696" alt="screenshot 2017-10-08 23 34 25" src="https://user-images.githubusercontent.com/20731901/31326081-4e556436-ac81-11e7-87d7-e9afeea2aaa4.png">

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

- Lines 91 - 137 of scripts.js file. I feel like this function could use much refactoring to make it cleaner and substantially shorter. I made an attempt throught my work on the project and ended up with a series of bugs or broken functionality. I would like to take more time to look over this code and figure out how to make it cleaner. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="1280" alt="screenshot 2017-10-08 16 24 34" src="https://user-images.githubusercontent.com/20731901/31321652-45476f96-ac46-11e7-9aec-f68cfe642ede.png">

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

- This project was a very great challenge for me. I often feel like it takes me more time than I have to wrap my head around how to approach tasks to have a well functioning project. I honestly did not think that I would make it though this project. I find I do work better in paired projects when I have someone to collaborate ideas with. Overall I am proud of the growth and learning that has taken place for me throughout the project and I need to remind myself to be more confident with the skills I have gained in a short period of time. 


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

## User Interface

**13 points**: The application shows effort in the interface, and is clean and minimal. The evaluator has some difficulty using the application when reviewing the features in the user stories.

* Click target is hard to see when locking a color in place because there is no hover effect/cursor change that indicates it's something I can click on. (This is a consistent problem, nothing looks clickable for any of the interactions on the page due to lack of hover effects and cursor changes.)

* The form flow for saving a new palette is slightly confusing. I know your solution closely mimics the wireframes, but wireframes are simply a guide, not something to be implemented and followed exactly to spec. Think about this flow from a user perspective, does it make sense to you? I initially tried to create a new palette and save it to a new project right away, but it seems this is a two-step process. After I create a new project, I'd immediately want to click 'save palette' and save it to that newly generated project, but instead it defaults to whatever is selected in the drop down on the left. I'd add more titles and descriptions of what you expect the user flow to be here to avoid confusion.

* Would be nice to get some user feedback when I try to add a project name with a duplicate title. As a user, it's hard to understand why this fails unless I'm explicitly told there already exists a project with that name.

## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database with correct relationships between folders and URLs.

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Pull requests are more important when you're collaborating in a group rather than working solo. You should still be using branches for your work (as you did), but using pull requests to merge them into master make the history difficult to read. All we see are these 'Merge Commits' that we have to dig into to actually see what functionality was added. If there's nobody reviewing your pull request, there's no point in creating one.

* Some instances of [commented out code](https://github.com/anajauregui/Palette-Pickr/commit/6114be75a324b0b2bfb2a7e2d0a50e254c9c6d2e#diff-22cbc1db13fa2c410616712446566a7cL40) that made it into master

* Some commits are doing a bit too much and the diffs are challenging to read. [This](https://github.com/anajauregui/Palette-Pickr/commit/6114be75a324b0b2bfb2a7e2d0a50e254c9c6d2e#diff-22cbc1db13fa2c410616712446566a7cL40) commit, for instance, is changing a lot of whitespace and semi-colon/code styling issues. These are things that should be broken out into separate commits so they don't clutter up the functionality that's being added.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
