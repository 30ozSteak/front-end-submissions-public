# BYOB Submission Form

[Project Spec](http://frontend.turing.io/projects/build-your-own-backend.html)


- **[<code>GET</code> /api/v1/merchants](https://byob-pam.herokuapp.com/api/v1/merchants )**
- **[<code>GET</code> /api/v1/merchants/:merchant_id](https://byob-pam.herokuapp.com/api/v1/merchants/125427)**
- **[<code>GET</code> /api/v1/products](https://byob-pam.herokuapp.com/api/v1/products)**
- **[<code>GET</code> api/v1/products/:id](https://github.com/500px/api-documentation/blob/master/endpoints/photo/GET_photos_id_comments.md)**
- **[<code>GET</code> /api/v1/merchantName](https://byob-pam.herokuapp.com/api/v1/merchantName?merchant_name=Sur%20La%20Table)**
- **[<code>PATCH</code> /api/v1/products/:id/edit](https://byob-pam.herokuapp.com/api/v1/products)**
- **[<code>PUT</code> /api/v1/products/:id/replace](https://byob-pam.herokuapp.com/api/v1/products)**
- **[<code>POST</code> /api/v1/merchants](https://byob-pam.herokuapp.com/api/v1/merchants)**
- **[<code>POST</code> /api/v1/products](https://byob-pam.herokuapp.com/api/v1/products)**
- **[<code>DELETE</code> /api/v1/merchants/:merchant_id](https://byob-pam.herokuapp.com/api/v1/merchants)**
- **[<code>DELETE</code> /api/v1/products/:id](https://byob-pam.herokuapp.com/api/v1/products)**

------

# Basics

#### Link to the Github Repository for the Project
[Build Your Own BE](https://github.com/thatPamIAm/build_your_own_be)

#### Link to the Deployed Application
[Deployed build on heroku](https://byob-pam.herokuapp.com/)

#### Link to Your Commits in the Github Repository for the Project

-[Commits](https://github.com/thatPamIAm/build_your_own_be/commits/development)

## Completion

#### Were you able to complete the base functionality?

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
[Code I'm proud of](https://github.com/thatPamIAm/build_your_own_be/blob/development/server.js#L101-L112)

* Why were you proud of this piece of code?

I'm proud that I was able to get the custom endpoint working, especially after having to use custom endpoints to hit the API I wanted for my project.

#### Link to a specific block of your code on Github that you feel not great about
[Meh code](https://github.com/thatPamIAm/build_your_own_be/blob/development/server.js#L146-L160)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I couldn't get my test for this endpoint to pass, which I believe has something to do with my using a unique column in my primary table as the foreign key in my secondary - as this is what the error continuously points to as being wrong.
## Testing
![](http://i.imgur.com/7vAZeG2.png)

## Linting

![](http://i.imgur.com/nLfjbhk.png)

-----

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----

## Instructor Evaluation Points (Robbie)

The following set of points are distributed at the discretion of the instructor.

### Endpoints

* **60 points** - Developer has implemented all 10 endpoints, 4 are secured via JWTs and one is a custom endpoint that filters data based on query params.
* **40 points** - Developer has implemented all 10 endpoints but did not secure 4 of them with JWTs or have a custom endpoint based on query params.
* **20 points** - Developer is missing endpoints and has not secured or customized any of the ones that have been implemented.

### Data Persistence with SQL Database

* **40 points** - The application persists data in a SQL database but with correct relationships between folders and URLs.
* **20 points** - The application persists data in a SQL database but with some incorrect relationships between folders and URLs.
* **0 points** - The application does not persist data in a SQL database.

### Testing & Linting

* **30 points** - Project has a running test suite that covers all happy and sad paths for the appropriate endpoints. The project has a linting configuration that passes with no errors.
* **20 points** - Project has a running test suite that covers most happy and sad paths for each endpoint. Linter has some errors that need fixing.
* **10 points** - Project has significant lack of testing for happy and sad paths of endpoints; Linter is failing on multiple lines.

### JavaScript Style

* **20 points** - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There _zero_ instances where an instructor would recommend taking a different approach.
* **15 points** - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.
* **12 points** - Your application has some duplication and minor bugs. Developer can speak to most choices made in the code and knows what every line is doing.
* **5 points** - Your application has a significant amount of duplication and one or more major bugs. Developer cannot speak to most choices and does not know what every line of code is doing.

- Points: x / 150