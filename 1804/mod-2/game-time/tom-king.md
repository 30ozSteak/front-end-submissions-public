# Game Time
* Students: Tom King
* Evaluator: Brittany Storoz

Comments:
* Nice work going solo, but don't use it as an excuse to do less ;) It's often actually faster and easier working alone than struggling through pairings, so instructors and future employers won't have much sympathy
* Testing was better after re-visiting it, use this project as a way to practice writing tests in the future and finish fleshing them out
* Demonstration of OOP skills is clear though code can be difficult to read at times -- there's a lot of complex logic here, but make sure you can still speak to it after graduation. An employer might ask you to talk through the code and I think you will have a hard time remembering exactly how it works (I would even if I wrote it). Create a branch for yourself with annotations for each line during an intermission/after graduation if you have to. 

### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* Level up extension in place by adding more missiles, good work!

### User Interface

* 3 - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

* Just needs a bit more instruction on keyboard shortcuts but otherwise easy to understand and play

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* Also [assert](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L31) that it's an instance of the Game class. (Do this for all test classes), there is syntax for that assertion specifically if you look through the mocha chai docs.

* [It should set instance properties appropriately](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L34) not store all the things

* Your descriptions like [this](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L85) are a little vague, and should be more geared towards explaining what the actual code is doing. e.g. "It should decrease the player's missile count when they shoot"

* Do you need to be calling [findBattery](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L129-L131) twice each time? This looks like something that should be refactored so that you can just call it directly in your assertion once.

* [This](https://github.com/tomkingkong/game-time/blob/master/test/Game-test.js#L141) isn't really asserting what you're describing. It looks like you're just testing that the game level gets updated after the loop.

* [I would break out setup like this](https://github.com/tomkingkong/game-time/blob/master/test/Weapon-test.js#L8-L20) into a separate file since you're repeating it across test files, then you can just import it in rather than having it in all those different places. 

### JavaScript Style & OOP

* 4 - Application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don’t repeat yourself) principles are utilized. There are zero instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.
* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* 1 - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated at all.


### Workflow

* 4 - The developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.
* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* 2 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* 1 - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* 0 - The application was not checked into version control.
