# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

* Fork this repo, if you haven't already and check out a branch
* Use this README as a template to create a file in this folder with your name as the title.
* Submit a pull request
* Pro Tip: You can use [recordit.co](http://recordit.co/) to record interaction gifs.
* Secondary Pro Tip: [Here's how to link to specific line number(s) in Github](http://stackoverflow.com/questions/23821235/how-to-link-to-specific-line-number-on-github)
* Tertiary Pro Tip: You can re-use some of these things in your portfolio/resume

------

# Basics

#### Link to the Github Repository for the Project
[Your projects's repo URL](https://github.com/zkc/antiqueBox)

#### Link to the Deployed Application
[Your project's production URL](https://antiquebox-stage.herokuapp.com/)

#### Link to Your Commits in the Github Repository for the Project

-[Commits - build branch](https://github.com/zkc/antiqueBox/commits/kz-build)

## Completion

#### Were you able to complete the base functionality?

* Seeded a database with at least 2 tables and 1 relationship?
(Yes)

* Had at least 10 endpoints that returned responses with appropriate status codes?
(Yes)

* Secured at least 4 endpoints with JWTs?
(Yes) - This is the first time I've ever had the problem where my tests PASS when they definitely should not. The JWT endpoints do function properly with manual testing.

* Enforced a linter and wrote code that conformed to it?
(Yes)

* Wrote tests for both happy and sad paths for each endpoint?
(~75% of current ep)

* Setup automatic deployments with CircleCI to a production app on Heroku?
(Yes)

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[Link to code block in repo](https://github.com/zkc/antiqueBox/blob/master/server.js#L33-L56)

* Why were you proud of this piece of code?

Initially I wasn't 100% sold on my choice to separating listings from individual items. This block gave me confidence that the division was a worthwhile. I'm proud of my mapping table that links items and listings.

#### Link to a specific block of your code on Github that you feel not great about
[Link to code block in repo](https://github.com/zkc/antiqueBox/blob/master/server.js#L118)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This is kind of a bug with knex, ultimately I want to reorganize this promise flow

## Testing

Attach a screenshot or paste the output from your terminal of the result of your test-suite running

<img width="533" alt="screen shot 2017-05-20 at 11 52 08 am" src="https://cloud.githubusercontent.com/assets/5368526/26278243/da8e614e-3d52-11e7-94ba-d34b1ffbc17f.png">
## Linting

Attach a screenshot or paste the output from your terminal of the result of your linter running

current lint output: 
<img width="654" alt="screen shot 2017-05-20 at 11 54 23 am" src="https://cloud.githubusercontent.com/assets/5368526/26278260/18e49e22-3d53-11e7-8638-112687cf6ee2.png">

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

May 21 - Added JWT. Came across a very wierd behavior where my tests pass despite the data clearly being different. 

May 20 - Built up more remaining base requirements besides JWT. Work continues. 

May 19 - I'm obviously not done with the project as of May 19. I will be continuing to work on this as I plan on building a front end and launching this site. This plan put me into a mindset where I felt compelled to make sure I was confident in my design decisions before progressing. Ultimately this created a reduction in priority of some elements of the assignment. Additionally I've had major job stress this week that I've yet to handle well and which hindered my progress. Overall I’m ecstatic to have a functioning pipeline, now I’m in a great place to be building up significantly more this weekend.

-----

# Instructor Feedback [Brittany]

* I evalled your master branch as that's what is linked to in the submission template. If you want credit for the changes you've made over the weekend, please make sure all your most recent code is pushed to master.

* Given that there is no front-end to this project, it would be nice to have a README that outlines all of the possible endpoints you can hit and each method they accept as mentioned in the [spec](http://frontend.turing.io/projects/build-your-own-backend.html).

## Feature Completion

### Endpoints
**25 points**: Developer has implemented 9 of 10 endpoints and did not secure 4 of them with JWTs and/or have a custom endpoint based on query params. Error handling was also very [weak](https://github.com/zkc/antiqueBox/blob/master/server.js#L29)/non-existent.

### Data Persistence with SQL Database
**40 points**: The application contains at least 2 tables with a proper relationship between data sources.

## Testing and Linting

**10 points**: Project has significant lack of testing for happy and sad paths of endpoints; Linter is failing on multiple lines.

* Even if you've run a `migrate:latest` locally to get your tests running, you still want to have that in your test file for other users that might want to pull down and run your tests. Your [beforeEach](https://github.com/zkc/antiqueBox/blob/master/test/routes.spec.js#L12-L16) should be refactored to look something more like this:

```js
before((done) => {
  database.migrate.latest()
    .then(() => {
      done();
    })
});

beforeEach((done) => {
  database.seed.run()
    .then(() => {
      done();
    })
});
```

* We didn't go over this in class, but in the future you could add linting to your CircleCI builds by adding the following to your `circle.yml` file (pretty common convention):

```json
test:
  override:
    - ./node_modules/.bin/mocha
    - ./node_modules/.bin/eslint
```

### JavaScript Style
**12 points**: Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* [Roar](https://github.com/zkc/antiqueBox/blob/master/server.js#L12)

* Remember that any number of things can go wrong within a request to a database, and we might not always be able to anticipate the error. In cases like [this](https://github.com/zkc/antiqueBox/blob/master/server.js#L24-L30) a 404 is a predictable error that we can use to respond with when we realize we have no results or an empty array. The `.catch()`, in that case, would have to handle literally every other thing that could have possibly gone wrong. Because we can't anticipate what went wrong, we'd want to respond with a 500 and the error message. Refactored, a proper way to handle this type of request and any errors might look like this:

```js
  database('listings').select()
  .then((listings) => {
    if (listings.length) {
      response.status(200).json(listings);
    } else {
      response.status(404);
    }
  })
  .catch((error) => {
    response.status(500).send({ error })
  });
```

* I'm a little confused about what's being returned [here](https://github.com/zkc/antiqueBox/blob/master/server.js#L39). Listing appears to be an object based on the line directly following your `.then()`, but you are wrapping it in an array?

* Even if you're not doing anything but console logs, make sure you always always have a `.catch()` block for [every](https://github.com/zkc/antiqueBox/blob/master/server.js#L103-L105) [single](https://github.com/zkc/antiqueBox/blob/master/server.js#L114-L119) [promise](https://github.com/zkc/antiqueBox/blob/master/server.js#L128-L130) [used](https://github.com/zkc/antiqueBox/blob/master/server.js#L162-L166)


## Points: 87 / 150


-------

Secondary Eval

* Testing is still very sparse
* Error handling is weak despite initial feedback in the first eval
* Has completed 10 endpoints
* Completed JWTs
* Master repo still contains a number of console.logs and commented out code
* Cannot determine if linter is passing or errors still remain as submission file has not been updated

* Endpoints: 60
* Data Persistence: 40
* Testing: 10
* JavaScript Style: 10

## Points: 120 / 150