# Palette Picker Submission - Jordan Quinn

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/JordanPQuinn/palette-picker)

#### Link to the Deployed Application
[heroku](https://jordans-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/JordanPQuinn/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Indeed I was!

#### Which extensions, if any, did you complete?
N/A

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/JordanPQuinn/palette-picker/blob/3751dbe3312b8bd273a5a14c5f3e2ded977e3464/public/js/scripts.js#L100)

* I really liked my approach for mapping the palettes back into their corresponding project here. I think it created a fun data structure to approach solving the rest of the problem with. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/JordanPQuinn/palette-picker/blob/3751dbe3312b8bd273a5a14c5f3e2ded977e3464/public/js/scripts.js#L100)

Ironically, my answer is the same. While I really like what I did in lines 100-104, I don't like the append methods. I think it was a little messier than it needed to be. I tried doing it all in one method with a bunch of nested maps and forEach's, which was definitely uglier than the finished submission. However, still not something I felt was particularly well executed. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
Palette Picker is running on 3000.
  Client Routes
    ✓ should return the homepage with text
    ✓ should return a 404 if the requested page is not found

  API Routes
    GET /api/v1/projects
Data seeded!
      ✓ should get all projects
    POST /api/v1/projects
Data seeded!
      ✓ should post a new project
Data seeded!
      ✓ should return a 422 with appropriate param message when no name is provided
    GET /api/v1/palettes
Data seeded!
      ✓ should return return all of the palettes
    POST /api/v1/palettes
Data seeded!
      ✓ should post a new palette
Data seeded!
      ✓ should return a 422 with appropriate param message when no name is provided
Data seeded!
      ✓ should return a 422 with appropriate param message when no colors are provided
Data seeded!
      ✓ should return a 422 with appropriate param message when no project id is provided
    DELETE /api/v1/palettes/:id
Data seeded!
      ✓ should return 204 on deleting a palette specified by an id
Data seeded!
      ✓ should return a 404 status code when the delete request fails due to an invalid id

#### Link to Design Inspiration

https://coolors.co/f7ebec-ddbdd5-ac9fbb-59656f-1d1e2c I just tried to recreate a very simple and clean UI, like coolers has. I like the way that coolers was able to generate complimentary colors to display the hex code. I opted for creating a nice transparent background behind them to make sure it stayed readable against darker colors.

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**45 points**: (50 possible points)

- Missing feature to click on a saved palette's colors and have the application display the colors on the main, top palette
- Everything else is good to go

## User Interface

**15 points**: (20 possible points)

- Not responsive (but this is not explicitly in the spec)
- Some buttons are overlapping slightly with neighboring input boxes
- Overall very pleasant, simple, and easy/clear to use
- I like the hex codes displayed over the palette colors (and the transparent background helps with darker palette colors)
- The scrolling container cuts off palettes when there are more than one and it isn't clear that the container is scrollable, but this is not a bit issue

## Testing

**16 points**: (20 possible points)

- I like [this comment](https://github.com/JordanPQuinn/palette-picker/blob/server-comments/test/routes.spec.js#L91) because it tells other developers what the intention of the test is

**- Missing a sad path for the DELETE endpoint (what happens if some sends a DELETE request to `/api/v1/palettes/10001` where the record 10001 does not exist in the database?)** 

- Good job testing the properties and values of each response body

## Commented Server File

**7 points**: (10 possible points)

- No comment [here](https://github.com/JordanPQuinn/palette-picker/blob/server-comments/server.js#L16), and this line should not be necessary for this project, which I think is why there is no comment
- For [this comment](https://github.com/JordanPQuinn/palette-picker/blob/server-comments/server.js#L12), I would say `environment variable` instead of just `environment` because the environment is more tied to production, dev, test, etc., but an environment variable is something more specific, like the PORT environment variable or the ENV environemtn variable, which hold the value of the current environment.
- [Here](https://github.com/JordanPQuinn/palette-picker/blob/server-comments/server.js#L32) the GET request has already been initiated, which is how we got to this endpoint, but the database query is being initiated
- Careful with wording [here](https://github.com/JordanPQuinn/palette-picker/blob/server-comments/server.js#L56), you aren't _posting_ to the DB, we are posting to the server, but we are _inserting_ into the database based on the POST request
- Again, overall good comments, just need to be a little more technically exact

## JavaScript Style

**23 points**: (30 possible points)

**- A 202 response is not quite the correct status code in [this case for DELETE](https://github.com/JordanPQuinn/palette-picker/blob/master/server.js#L84). If we look at the definition of a [202](https://httpstatuses.com/202), it means that the request will be finished at a later time, but by the time you have sent the response, the record has already been deleted from the table. You can use a 200 status code or 204 status code if you are not sending content back in the response.**

- [This HTTPS redirect](https://github.com/JordanPQuinn/palette-picker/blob/master/server.js#L14-L20) isn't necessary for this project...but would be good to have if you were making this application into a progressive web app
- A good next step would be to extract [this](https://github.com/JordanPQuinn/palette-picker/blob/master/server.js#L35-L41) and other parameter checking into their own middleware function that can be reused
- Need to be able to handle an unknown ID for the DELETE endpoint (as mentioned in the testing section above), should send a 404 status code for an unknown ID

**- [This endpoint](https://github.com/JordanPQuinn/palette-picker/blob/master/server.js#L24) should be plural, `projects` instead of singular project - same with the POST endpoint**

**- Along those lines of the endpoint being plural, the table names can be singular or plural based on your development teams style, but usually plural is preferred. Your `project` table is singular, but the `palettes` table is plural. Be consistent here - [make the project table plural](https://github.com/JordanPQuinn/palette-picker/blob/master/db/migrations/20180517193729_initial.js).**

## Workflow

**15 points**: (20 possible points)

- Like you said, commits were very large, and we like to see small, atomic commits (does your team have small commits and then squash them, or do you just commit very infrequently?)
- Be sure to add `.DS_Store` to your `.gitignore` file if you're working on a Mac


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 121 / 150

