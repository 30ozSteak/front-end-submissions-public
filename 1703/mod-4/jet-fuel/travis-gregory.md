# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/tlgreg86/jet-fuel)

#### Link to the Deployed Application
[heroku](https://tg-jetfuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/tlgreg86/jet-fuel/blob/083bb0ee41d05e207981fa2a29a8ff4310316e0b/server.js)
* I ran out of time and didn't get to annotate my server file.

## Completion

#### Were you able to complete the base functionality?

I wasn't able to get to the point of sorting the data and I didn't get the urls add date formatted the way I wanted because I just had a difficult time getting through testing and getting the routes and backend hooked up. I also couldn't get the redirect route to pass in testing. Those are the only pieces I wasn't able to complete, that I know of at least.

#### Which extensions, if any, did you complete?

I didn't get far enough to do any of the extentions.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/tlgreg86/jet-fuel/blob/8dbf6f42f06cfec1e8a972b411e959a5ffc60852/server.js#L30)

* This part just took me a while to get working correctly and it felt good to get it down.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/tlgreg86/jet-fuel/blob/8dbf6f42f06cfec1e8a972b411e959a5ffc60852/public/scripts.js#L134)

* This code is just really ugly and I found it to be difficult just dealing with all of the conditionals involved with the regex.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]

travis: jet-fuel (master) >> npm test

> jet-fuel@1.0.0 test /Users/travis/Documents/Turing/4-Mod/projects/jet-fuel
> mocha

Jet Fuel is running on http://localhost:3000.
  Client routes
    ✓ should return the homepage (46ms)
    ✓ should return error 404 if route does not exist

  API Routes
    GET /api/v1/folders gets all folders
      ✓ should return an array of folders
    POST /api/v1/folders adds to folders
      ✓ should create a new folder
      ✓ should not create a folder if a parameter is missing
    GET /api/v1/folders/:id/urls
      ✓ should return all urls
    POST /api/v1/folders/:id/urls
      ✓ should create a new url
      ✓ should not create a url with missing parameters
    GET /api/v1/urls/:id
      - should return the original url


  8 passing (299ms)
  1 pending

#### Please feel free to ask any other questions or make any other statements below!

This project was really difficult for me and though I got through most of it I did not get so far as to comment out my server file. I would still like to do it if I'm allowed.

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**40 points**: There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.

## User Interface

**12 points**: The application shows effort in the interface, but some aspects of the UI make the interactions confusing. The evaluator has some difficulty using the application when reviewing the features in the user stories.

* Tough to tell that I've successfully created a new folder, I see it's added in the drop down but there's no other visial indication that the request succeeded.
* It's bizarre that you can't see the folders or links until you select a folder from the drop-down menu. I wouldn't have that form element controlling a display element. It should simply be for selecting a folder to create a new URL. Especially when the message about clicking on the links below is persistent.  It's also hard to tell what folder is being displayed because it's simply a list of the URLs with no folder container or header.
* It's tough to tell that the submit button is disabled due to an invalid URL. I'd like some indication of what I did wrong (an error message or something) when I enter an invalid URL so that I can fix it.

## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database but with correct relationships between folders and URLs.

* [Long url](https://github.com/tlgreg86/jet-fuel/blob/master/db/migrations/20170816184259_initial.js#L13) doesn't necessarily need to be unique here. You might want to put the same long URL in multiple folders.

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**14 points**: The developer makes a series of small, atomic commits that document the evolution of their application. There are some formatting issues in the code base.

* Good use of branches all appropriately named
* ~40 commits likely isn't enough for the scope of this project. I'd likely expect somewhere in the 100s. This low number is an indicator that your commits are all likely doing a little too much and should be broken out into further commits.
* Some [instances](https://github.com/tlgreg86/jet-fuel/commit/f6d491a62b5d1e1cf5e53a8da6a784cad2bc179d) of commented out code being committed to the repo
* Don't commit [WIPS](https://github.com/tlgreg86/jet-fuel/commit/c1973dc638326d1b4ab912cde1b30547bec3f256) to master. This commit also does a bit more than the commit message implies. The diff is still easy to read, but there are irrelevant additions in this changest (get request)

### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
