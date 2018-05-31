# Instructor Evaluation Points - weathrly
# Instructor: Leta
# Comments:
  * No need to bind the componentDidMount - you don't need to bind any lifecycle methods (componentDidMount, render, etc)
  * Also no need to bind the cleaner functions; they don't reference `this` anywhere, so binding them is unnecessary!
  * If you use the `geolookup` weather underground endpoint, you won't need to clean your location data :)
  * Refactor the hourlyCard and the dayCard into a single component that leverages conditional rendering
  * In App.test.js, that first test implies that you'll be checking all 3 pieces of state, but only checks one. Be detailed and verbose when testing :)
  * In App.test.js, nice job testing the conditional rendering
  * *Testing is incomplete; if a passing score is desired, please complete by 11:59pm on Friday*

## Specification Adherence

Score: failing - pending implementation of autocomplete

4 - The application meets all of the requirements listed above and implements one or more of the extensions.

3 - The application consists of one page with all of the major functionality being provided by React. No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

2 - The application is in a usable state, but is missing 1 or more of the features outline in the specification above.

1 - The application is missing 3 or more smaller features or 1 major feature essential to having a complete application.

0 - The application is unusable.

## User Interface

4 - The application is pleasant, logical, and easy to use. The application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality and the application stands on it own to be used by the instructor without guidance from the developer.

3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality. The application less than 3 aXe-core violations

2 - The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the user stories.

1 - The application is confusing or difficult to use.

## HTML Style

_4 - Developer is able to craft HTML that is semantically correct and clearly organized. There are zero instances where an instructor would recommend taking a different approach. Developer writes markup that is exceptionally clear and well-factored. Application is expertly organized and logically structured with with a clear, thoughtful use of tags and selectors._

*3 - Developer solves structural problems with a balance between conciseness and clarity. Developer can speak to choices made in the code and knows what every line of code and every tag and selector is doing.*

_2 - Developer writes effective HTML, but does not write semantically correct and clearly organized code. Application shows some effort to use semantically correct HTML, but the divisions are inconsistent or unclear. There are many un-semantic tags and unnecessary selectors and it is not clear to the evaluator what a given section of code represents visually. Developer cannot speak to every line of code._

_1 - Developer writes code with unnecessary tags, selectors, or nesting which do not increase clarity. Developer writes code that is difficult to understand. Application markup shows poor structure with no understanding of semantics._

## CSS/Sass Style

_4 - Application has exceptionally well-factored CSS/Sass with little or no duplication and all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach._

*3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of CSS/Sass is doing.*

_2 - Your application has some duplication and minor bugs. Developer can speak to most choices made in the code and knows what every line is doing._

_1 - Your application has a significant amount of duplication and one or more major bugs. Developer cannot speak to most choices and does not know what every line of CSS/Sass is doing. Developer writes code with unnecessary selectors or tags which do not increase clarity._

## JavaScript / React Style

Pending refactor of cards into a single Card class

4 - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture.

3- Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application has at least 6 components built out.

2 - Your application has some duplication and minor bugs. Developer can speak to most choices made in the code and knows what every line is doing. The application has large components and logic could be broken out to smaller stateless components.

1 - Your application has a significant amount of duplication and one or more major bugs. Developer cannot speak to most choices and does not know what every line of code is doing.

0 - Your client-side application does not function or the application does not make use of localStorage for updating information on the client. Developer writes code with unnecessary variables, operations, or steps which do not increase clarity.

## Testing & Sanitation

Score: failing - refactor due by 11:59pm.

4 - Project has a running test suite that exercises the application at multiple levels (feature and unit). The test suite covers almost all aspects of the application. ESLint shows 0 complaints.

3 - Project has a running test suite that tests and multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of feature testing. ESLint shows less than 5 complaints.

2 - Project has sporadic use of tests and multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows more than 5 complaints.

1 - There is little or no evidence of testing in this application. ESLint shows more than 10 complaints.

## Workflow

_4 - The developer effectively uses Git branches and many small, atomic commits that document the evolution of their application._

*3 - The developer makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base.*

_2 - The developer makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application._

_1 - The developer committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application._

_0 - The application was not checked into version control._
