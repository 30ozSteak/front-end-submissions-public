# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/lolakoala/palette-picker)

#### Link to the Deployed Application
[heroku](https://lolas-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/lolakoala/palette-picker/tree/comments)

## Completion

#### Were you able to complete the base functionality?

Yes! 

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?

I did not complete any extensions.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L21-L42)

* Why were you proud of this piece of code?

Each project gets it's own palettes on page load, and then puts the colors of each palette into an array. I map through the array to create an html tag for each color, and then I append it to the page. I thought this was a sleek solution to appending the color palettes.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L66-L94)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

In this code, I'm toggling the lock img attributes on click of both the color div and the image. I expected it to work on the img (which is inside the div) without having to code it on click due to event bubbling... When it did not behave as expected, I basically had to duplicated some code and change the selector. I was nervous about refactoring this into one function because the code is just different enough that I'm not sure what I would pass in to handle that.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

12 passing (513ms)
  1 failing

  1) Uncaught error outside test suite:
     Uncaught Error: listen EADDRINUSE :::3000


#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[art bag image](https://dribbble.com/shots/313499-Artist-Bag-Icon)

I was inspired by this image to make my app art-themed. I envision my app being used by art students/teachers.

[circles image](https://dribbble.com/shots/1710723-Brawker-The-new-color-palette)

I use a lot of circles and rounded corners in my designs, but these circles really helped me envision how I wanted the random color palette to look. I found this before the art supplies bag, so when I found that I ended up placing the circles on the paint palette image.

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

The design of this project was a lot of fun! I am enjoying learning about the backend. 

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**40 points**: (50 possible points) There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.

* I'm noticing when I click on a lock icon, it doesn't actually lock the color in place. Every time I generate a new palette, it continues to change all 5 colors.

* When I click on a pre-existing palette that has been saved, it should update the main palette UI to display those colors. Doesn't seem to be doing that at the moment.

## User Interface

**16 points**: (20 possible points) User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.

* Creative UI! Love the paint palette. The lock icons are maybe a little difficult to decipher...I think if I didn't have any context on the project I'm not sure I would know they were locks that I could/should click on.

* When there are no projects in place, the drop down menu for selecting a project is completely empty. Would be nice to have a placeholder here at least that says something like 'Select a Project...' even if there were no projects to choose from. Otherwise it's a little tricky to tell what that drop-down is for.

* When I first start filling out the projects panel with new projects, the project name shows up all the way at the bottom of that div which looks a little bizarre. It fills out nicely once there are about 5 projects in place, but it'd be nice to have everything looking solid no matter what amount of data you have in place. 

* You generally want to avoid having little containers (like the projects element) that have vertical and horizontal scroll bars. I know you don't have a ton of control over the vertical height of the projects section, but the horizontal you could probably remove that extra scrollbar with `overflow: hidden`, and put a limit on the length of a project/palette name. Set a fixed width (or all percentage-based widths) on that element and all of it's children to ensure the width isn't bouncing around based on what kind of content exists.

## Testing

**19 points**: (20 possible points) Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

* [This](https://github.com/lolakoala/palette-picker/blob/master/test/routes.spec.js#L157-L178) is a scenario in your testing environment where you wouldn't hardcode in an ID. The user doesn't pass in an ID from the front-end, so don't pass one in in your test. You can still POST a new palette, and assert that the response body has an `id` property, just leave out the assertion of what that ID value is. Same thing [here](https://github.com/lolakoala/palette-picker/blob/master/test/routes.spec.js#L109-L122)

* Nice job asserting against [error messages](https://github.com/lolakoala/palette-picker/blob/master/test/routes.spec.js#L135) and not just status codes.

## Commented Server File

**10 points**: (10 possible points) Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity

## JavaScript Style

**22 points**: (30 possible points) Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* Loveeeeeeeee that you broke this [checkParams](https://github.com/lolakoala/palette-picker/blob/master/server.js#L8) out into a helper file.

* I believe you could just use a `unique()` method in your migration file on the name column for your schema rather than having to do this entire [check](https://github.com/lolakoala/palette-picker/blob/master/server.js#L59-L67) for duplicate names.

* I'm torn on [this](https://github.com/lolakoala/palette-picker/blob/master/server.js#L105-L107) being a 422 over a 404. If the error is that a resource doesn't exist at that endpoint, it should be a 404. 422's are more commonly seen when you're passing through an actual request body.

* You don't want to be [appending to the DOM](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L38-L40) on each iteration of a for loop. DOM manipulations are expensive. Instead, you'd want to use Document Fragments to build up all the HTML you want to append, and then add it to the DOM all at once at the end of the loop.

* Rather than swapping out an image [here](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L66-L78) you could maybe use that icon as a transparent background image so that you only have to toggle a class instead.

* I'd save [this jQuery selector](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L84-L92) as a variable so that jQuery only has to traverse the DOM once in order to find it. Traversing the DOM is expensive and if you save it in a variable you only have to perform that search once.

* Fetch requests arent dependent on the [DOM](https://github.com/lolakoala/palette-picker/blob/master/public/scripts/scripts.js#L167) so this function shouldn't be waiting for the whole window to load before you kick it off. Get that data ASAP.

## Workflow

**17 points**: (20 possible points)

* In general, you probably want to be committing a bit more frequently. For a project of this size and scope you definitely want to have over 100 commits, at least. Having less than that is usually indicative of having really large diffs that are difficult to read. Like [this](https://github.com/lolakoala/palette-picker/commit/660c6fc08c5cdcdd0a1ce0759b131b0f9e6f86dc) one ;)

* Try working with github issues to keep track of your to-do list for functionality/bug fixes/design issues/etc. Pull requests aren't necessary when you're working individually, they're more for code review when you have other teammates that need to approve your changes.

### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 124 / 150
