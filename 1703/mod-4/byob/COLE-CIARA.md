# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/buji405/byob)

#### Link to the Deployed Application
[Heroku](https://craft-brewz.herokuapp.com/)


## Completion

#### Were you able to complete the base functionality?

* Documented all available endpoints and their usage in the README?
Yes

* Seeded a database with at least 2 tables and 1 relationship?
Yes

* Had at least 10 endpoints that returned responses with appropriate status codes?
Yes

* Secured at least 4 endpoints with JWTs?
Yes

* Enforced a linter and wrote code that conformed to it?
Yes

* Wrote tests for both happy and sad paths for each endpoint?
Yes

* Setup automatic deployments with CircleCI to a production app on Heroku?
Yes

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/buji405/byob/blob/master/src/router.js#L1-L22)

* Why were you proud of this piece of code?

This definitely helped us simplify our endpoints. By separating this piece of code we were able to create cleaner and more modular code. This allowed us to trace errors and update any functionality with greater ease.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/buji405/byob/blob/master/src/controllers/BreweriesController.js#L40-L67)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Functionally this code works great, however, there is a lot of nexted promises and knex queries that could be separated into cleaner functionality. Also, although we split out our code into separate controllers, I feel there are even better ways we can separate our code to make everything single responsibility.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/buji405/byob/blob/master/public/images/test-suite.png)

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

[linter output](https://github.com/buji405/byob/blob/master/public/images/linter.png)

#### Attach a screenshot of your CircleCI build passing

[circleCI build](https://github.com/buji405/byob/blob/master/public/images/circle-ci-build.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Great project - definitely taught us a ton about the complexities that go into an API, and we barely scratched the surface!

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**10 points**: The README includes documentation for all available endpoints and how to use them. Instructor can easily follow the documentation for using the API.

### Feature Completion

**x points**: Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**35 points**: Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. Error handling is informative and helpful for the end-user. The project has a linting configuration that passes with no errors.

* If you're setting the test environment [here](https://github.com/buji405/byob/blob/master/package.json#L7), you shouldn't need to hardcode the word 'test' [here](https://github.com/buji405/byob/blob/master/test/routes.spec.js#L3). Keeping that configuration dynamic would allow you to break out those two lines into a helper file and import it directly into your server and test files.

* You could rewrite [this line](https://github.com/buji405/byob/blob/master/src/server.js#L19) to be just `module.exports = app` and then you wouldn't have to use this weird syntax in your [test file](https://github.com/buji405/byob/blob/master/test/routes.spec.js#L7)

* I'd be careful about expiring a test JWT in [2 minutes](https://github.com/buji405/byob/blob/master/test/routes.spec.js#L15). The more complex your API gets, the more likely it will take longer than 2 minutes for your test suite to run.

* [First things first](https://github.com/buji405/byob/blob/master/test/routes.spec.js#L36-L45), always always always have a `.catch()` with your `.thens()`. Second, don't do rollbacks on your schema during your tests. This puts your database in an out-of-date version and you'll be testing against the wrong things. You're undoing this by migrating latest immediately after the rollback any way, so it's not really giving you anything useful.

* I'd make your it blocks a little more [descriptive](https://github.com/buji405/byob/blob/master/test/routes.spec.js#L67). I can't tell what POST request this is testing until I look a couple lines down to the actual request. Happy/Sad Path terminology is something we use when we're discussing the types of tests we write, but they're not the most helpful in our test descriptions.




### JavaScript Style

**x points**: Lorem ipsum dolor set amet


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
