# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the GitHub Repository for the Project
[BYOB](https://github.com/johnmboudreaux/BYOB)

#### Link to the Deployed Application
[Heroku](https://jm-byob.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
(Yes)

* Seeded a database with at least 2 tables and 1 relationship?
(Yes)

* Had at least 10 endpoints that returned responses with appropriate status codes?
(Yes)

* Secured at least 4 endpoints with JWTs?
(Yes)

* Enforced a linter and wrote code that conformed to it?
(Yes)

* Wrote tests for both happy and sad paths for each endpoint?
(Yes)

* Setup automatic deployments with CircleCI to a production app on Heroku?
(Yes)

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code]()

We feel very good about our entire server.js file. With everything being a turnary as well as being dirct readable code we feel that it is all well done. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code]()

The code we feel could use a bit more love is the fron end side of things. While it fits all the requirements it is not the most clean user friendly front end code we have done. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="937" alt="screen shot 2017-12-17 at 4 03 55 pm" src="https://user-images.githubusercontent.com/26842728/34084815-f39a99fe-e343-11e7-85c4-fd4569703551.png">

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

<img width="701" alt="screen shot 2017-12-15 at 12 28 35 pm" src="https://user-images.githubusercontent.com/26842728/34057296-9ce32952-e193-11e7-9df5-4dd7c4ff7eb8.png">

#### Attach a screenshot of your CircleCI build passing

<img width="1169" alt="screen shot 2017-12-15 at 12 24 28 pm" src="https://user-images.githubusercontent.com/26842728/34057118-f97622f6-e192-11e7-97fe-0273cfda7412.png">

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**9 points**: The README includes documentation for all available endpoints and how to use them. Instructor can easily follow the documentation for using the API.

* Nice [intro paragraph](https://github.com/johnmboudreaux/BYOB#by-ben-porter-and-john-boudreaux)

* Good formatting, easy to read and follow along with

* Would like you to be just a littleeee more explicit about data types for your [POST and PATCH requests](https://github.com/johnmboudreaux/BYOB/blob/master/docs/POST_owners.md#request-body). I can infer based on the request body example, but it would be nice for you to explicitly tell me the data types as well.

### Feature Completion

**x points**: (60 possible points) Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: (40 possible points) Lorem ipsum dolor set amet

### JavaScript Style

**x points**: (40 possible points) Lorem ipsum dolor set amet

### Workflow

**17 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Would be good to see some use of github issues for tracking what needs to be done

* Formatting of commit messages is a littleeeee inconsistent in terms of capitalization/tense

* Generally you don't want to commit [generated source code](https://github.com/johnmboudreaux/BYOB/commit/ff7d10bbf407e4f29fa405e48a9b32aca8f89b9a#diff-fae01302d764057eca5e4bfaa4bfbaa4) like bundle files. This causes a lot of headaches and unecessary merge conflicts when collaborating with other developers. You leave code generation like this to the server (e.g. on heroku, you might use a build pack or add a command in your Procfile that tells the server to run a webpack build of your codebase and generate the bundle file on the fly.)

## Project is worth 170 points

## To get a 3 on this project, you need to score 125 points or higher
## To get a 4 on this project, you need to score 145 points or higher

# Final Score: x / 170
