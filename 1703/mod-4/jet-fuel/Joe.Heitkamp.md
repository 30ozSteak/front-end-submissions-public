# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/noetic97/jet-fuel)

#### Link to the Deployed Application
[heroku](https://joes-jet-fuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/noetic97/jet-fuel/blob/server-descriptions/server.js)

## Completion

#### Were you able to complete the base functionality?

Mostly.  You can not filter the links by date and the date is not showing next to the links.  I underestimated the time it would take to complete the testing, and did not finish implementing all the UI.

#### Which extensions, if any, did you complete?

* All of the client-side interactions are tested

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/noetic97/jet-fuel/blob/master/test/routes.spec.js)
Line 250-258
``` response.body.map((link) => {
          link.should.have.property('id')
          link.should.have.property('description')
          link.should.have.property('ogURL')
          link.should.have.property('shortURL')
          link.should.have.property('folder_id')
          link.should.have.property('created_at')
          link.should.have.property('updated_at')
        })```

* It was a simple solution to testing multiple links without having to test each link by hand.  I wasn't sure if it was possible to map and then test over each result, but it worked right away!

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/noetic97/jet-fuel/tree/master/db/migrations)

* I do not like having these accidental migrations that now throw warnings in my test results.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]
```Client Routes
    ✓ Should return the home page with text (38ms)

  API Routes
    GET /api/v1/folders
Knex:warning - migration 20170818120129_initial.js did not return a promise
Knex:warning - migration 20170818120143_initial.js did not return a promise
Knex:warning - migration 20170820002113_add.js did not return a promise
      ✓ Should return all folders in the DB
    POST /api/v1/folders
      ✓ Should add a new folder to the DB
      ✓ SAD PATH - Should return an error message if the folder is missing title
      ✓ SAD PATH - Should not allow a user to add a folder if it already exists
    GET /api/v1/folders/:id
      ✓ Should return a specific folder in the DB
      ✓ SAD PATH - Should return an error message when an improper id is passed in
    GET /api/v1/links
      ✓ Should return all links in the database
    POST /api/v1/links
      ✓ Should add a new link to an existing folder
      ✓ SAD PATH - Should return an error message when an improper parameter is passed in
    GET /api/v1/folders/:id/links
      ✓ Should return all of the links to a specified folder


  11 passing (368ms)```

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

* Ahhhhh the blue is burning my retinas.
* There is a lot of low-hanging fruit here that could significantly improve the front-end. Spend some time picking a font and adding some padding to the content so it's not so flush-left. I know time is always an issue with these projects, but remember that you're a front-end developer and these are the things you'll be showing in your portfolio to employers. This particular UI doesn't seem to demonstrate a solid effort.

## Data Persistence with SQL Database

**15 points**: Mostly set up the database with the correct relationships and fields though there are a lot of inaccuracies and inconsistencies throughout the migrations directory.

* Not sure how you ended up with so many duplicate [migrations](https://github.com/noetic97/jet-fuel/tree/master/db/migrations), but in the future you should do a rollback all the way to the beginning and remove those.
* Nice column [name](https://github.com/noetic97/jet-fuel/blob/master/db/migrations/20170816142930_initial.js#L14)
* The [shortUrl](https://github.com/noetic97/jet-fuel/blob/master/db/migrations/20170816142930_initial.js#L15) must be a unique value. If you generate two of the same short URLs, that point to different long URLs, one of them will be overridden. 
* The up and down in [this](https://github.com/noetic97/jet-fuel/blob/master/db/migrations/20170821011902_add-unique-folder-param.js) migration don't match. The down should do exactly the opposite of what the up does. Trying to rollback past this point would put your database into a bad state.

## Testing


**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**13 points**: The developer makes a series of small, atomic commits that document the evolution of their application. There are some formatting issues in the code base, some commits are taking on too much responsibility.

* Commits like [this](https://github.com/noetic97/jet-fuel/commit/3f1e9ca23b0da1f4c8f7d16dc3a6703de4106ecf) are doing a bit too much. Based on the message I'd be expecting only to see server-side code in this commit, definitely not CSS.
* ~35 commits isn't enough for a project like this, you likely want to be at around 100 at least. Your commits should do much less than they currently are.
* [This](https://github.com/noetic97/jet-fuel/commit/909ca1b7e07687c0b220d95ffaf36db1bdbf9616) might be the most uninformative commit message I've ever seen
* You want to .gitignore these [DS_Store](https://github.com/noetic97/jet-fuel/blob/master/db/.DS_Store) files


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
