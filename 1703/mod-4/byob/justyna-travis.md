# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)

------

# Basics

#### Link to the Github Repository for the Project
[BYOB](https://github.com/JustynaField/BYOB)

#### Link to the Deployed Application
[Heroku](https://jw-byob.herokuapp.com/)


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
[happy code](https://github.com/JustynaField/BYOB/blob/aa749f174f5d05d565789cdbf01616a0505ee8ca/test/routes.spec.js#L124)

* Why were you proud of this piece of code?
It was difficult figuring out how to test authentication. We were happy when we figured out how to do it.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/JustynaField/BYOB/blob/master/data.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We are not feeling great about not being able to scrape the data we needed for this project. The data we found was contained in a table, withought any class or id assigned to td's.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
Client Routes
    ✓ should run homepage with text (44ms)
    ✓ should return 404 for a route that does not exist

  Authentication
    ✓ should allow user access if user submits app name and email address ending with @turing.io
    ✓ should not process the request if one parameter is missing

  API Routes
    GET /api/v1/brewery
      ✓ should return all of the breweries
    GET /api/v1/brewery/:id
      ✓ should return a brewery by id
      ✓ should return an error if a requested brewery does not exist
    POST /api/v1/brewery
      ✓ should create a new brewery
      ✓ should not create a record if "name" parameter is missing
    PATCH /api/v1/brewery/:id
      ✓ should update a specific brewery
      ✓ should not update a brewery without the required parameter of name
    GET /api/v1/beer
      ✓ should return all beers
    GET /api/v1/beer/:id
      ✓ should return beer by id
      ✓ should not return beer that does not exist
    GET /api/v1/brewery/:id/beer
      ✓ should get all beers for a specific brewery
      ✓ should return no beers if id is not found
    POST /api/v1/brewery/:id/beer
      ✓ should post beer to a specific brewery
      ✓ should not post a beer missing required parameters
      ✓ should not add a beer if the id does not exist 
    DELETE /api/v1/brewery/:id/beer
      ✓ should delete all beers for a specific brewery
      ✓ should not delete a beer if the brewery does not exist
    PATCH /api/v1/beer/:id
      ✓ should update a specific beer
      ✓ should not add a beer if id does not exist
    DELETE /api/v1/beer/:id
      ✓ should delete a specific beer
      ✓ should not delete beer if it does not exist


  25 passing (645ms)
```

#### Attach a screenshot or paste the output from your terminal of the result of your linter running.

```
/Users/justyna/turing/mod4/BYOB/db/migrations/20170822140650_initial.js
  19:36  error  Trailing spaces not allowed  no-trailing-spaces

✖ 1 problem (1 error, 0 warnings)
  1 error, 0 warnings potentially fixable with the `--fix` option.
```
```
> BYOB@1.0.0 lint /Users/justyna/turing/mod4/BYOB
> eslint ./
```

#### Attach a screenshot of your CircleCI build passing

[circleCI build](http://i.imgur.com/g8Fd6aL.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say

-----


# Instructor Feedback (Brittany)

The following set of points are distributed at the discretion of the instructor.

### Documentation

**5 points**:  The README documentation is sparse in the information it provides and formatted in such a way that the instructor can not easily use every endpoint based on following the documentation.

* The 'requires authentication' notes you've added to your write request documentation is really vague. What do I actually do to my request in order to authenticate it?

* The formatting of the documentation makes it pretty difficult to follow. I'd like to see broken out lists of required/optional parameters for write requests that tell me the name, required/optional, a description and the data type of each parameter. I wouldn't be able to do a POST request following [this](https://github.com/JustynaField/BYOB#post-apiv1breweryidbeer) documentation.

### Feature Completion

**x points**: Lorem ipsum dolor set amet

### Testing & Linting & Error Handling

**x points**: Lorem ipsum dolor set amet

### JavaScript Style

**x points**: Lorem ipsum dolor set amet


## Project is worth 150 points

## To get a 3 on this project, you need to score 110 points or higher
## To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
