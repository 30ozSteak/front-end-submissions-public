## Student: Mike D and Jon
## Evaluator: Pamela Lovett
## Notes/What To Work On:

### DESIGN/COMP
- Nice work getting through most of the project. Cards can be generated with empty fields for title/body. 
- Stays true to the spirit of the comp - looks pretty good!

### HTML
- Good job using labels - next time use  `aria-label` attribute on inputs instead of label elements (since you are not using a visible label)
- Correct your path in line 26 so that jquery loads as backup, if needed
- Nice work using alts on your dynamically generated cards. Most of the application does well when run through VoiceOver. Be sure to run your app through a screen reader every time!

### CSS
- Declarations, at a minimum, should be organized alphabetically within selectors. Next time, try using [Idiomatic CSS](https://github.com/necolas/idiomatic-css) for organizing declarations
- Note that setting the `font-size` in px (line 4) runs into accessibility issues - as it will override any browser settings set by the user. Setting this to a percentage avoids this. 62.5% would be the equivalent of 10px. See [this](https://engageinteractive.co.uk/blog/em-vs-rem-vs-px) article for a more detailed explanation
- Remove any empty selectors
- Nice work grouping elements with the same declarations

### JS
- Good job speaking to most of your code
- Be sure to use `var` before initializing your variable `i` in the loop on line 7
- Use named function for event listener on line 16 as opposed to using anonymous function
- Nice use of the data attribute for storing your ids in line 67
- Unneccessary use of pulling text from DOM in lines 73, 77, 86, and 89 for `changeQualityUp/Down`. Check the property from the `parsedIdea` that you pull for your expression (shown below). No need for `else if` as there are only two options (an `else` for the second condition would work fine). Update text on DOM outside of conditional before sending to local storage to reduce redundant lines.

```js 
  if (parsedIdea.quality === 'swill') {
    ...
  }
``` 
- `persistTitleEdit` & `persistBodyEdit` could be refactored into one function

### GIT/GITHUB

- Made it so that reviews  were required in settings for GitHub!!
- Yay for comments in PR!!!
- Good number of commits 
- Capitalize first letter in commits - be more descriptive in some


## Functional Expectations

* Proficient  The application consists of one page with all of the major functionality being provided by jQuery. No approach was taken that is counter to the spirit of the project and its learning goals.

## HTML

## Accessibility

* Proficient  Employs detailed accessibility practices throughout markup, especially in forms and can speak to decisions made in accessibility choices as it relates to specific accessibility concerns.
* Exceptional Can run markup through a variety of online accessibility tools and score well for content, color, screen readers, etc.

## Style

* Proficient  Crafts lean, efficient markup that is easy to read and follow across naming conventions, structure, and solid formatting that follows industry best practices.

## CSS

## Structure of Code

* Advanced Beginner Can cleanly and logically organize CSS rules according to similar categories (i.e. typography, layout, components), and then logically organize the remaining CSS rules based on flow of the markup. Organizes properties within rules alphabetically.

## Implementation

* Proficient  Develops layouts that work cross-browser, are responsive, and can logically defend the choices made in implementation approach for layout.

## JAVASCRIPT

## Data Types

* Proficient  Can identify and track data types through any variety of functions, understanding their affect and result on each line of code. Knows which scenarios are better suited for objects vs. arrays and employs them accordingly.

## Conditional Logic

* Proficient  Can use an if/esle statement to effectively handle multiple paths through the code. Writes if/else statements that only have one level of logic (no nesting). Can use logical operators instead of if/else statements where applicable.

## Functions & Scope

* Proficient  Functions have single responsibility. The entirety of the function is easy to read what functionality it contains. Function is generally shorter than 8 lines. Uses functions to eliminate repeated code. Comfortable refactoring any piece of code and extracting it to a function.

## Arrays

* Advanced Beginner Can modify arrays by adding or removing specific elements - uses array methods such as push or shift. Can use a for loop to iterate through array.
* Proficient  Does not use for loops for arrays - uses array prototypes, such as forEach, to iterate through or manipulate arrays. Can use array to store more complicated data structures such as objects or nested arrays. Is comfortable/efficient with reading array prototype documentation and can efficiently test/apply array prototype methods they have not worked with before.

## Objects & Prototypes

* Advanced Beginner Can use object constructor functions and is comfortable with extracting values of properties on different object instances.
* Proficient  Can use object prototypes. Can articulate the definition and the “why” of an object prototype - the best use cases for prototypes.

## DOM Manipulation
* Proficient  Able to extract information, modify attributes, or append/prepend data in the DOM easily regardless of whether they are employing vanilla JavaScript or jQuery. Understands how to harness event bubbling.

## Style

* Proficient  Code is logically organized, such that reader can easily follow the progression of the app because variable and function names are descriptive and follow a single responsibility approach. There are no major bugs and minimal duplication.

## GIT & GITHUB

## Git

* Proficient  Commits changes frequently with detailed commit messages. Uses feature branches to keep master branch free of incomplete features or bugs.

## GitHub
* Proficient  Is comfortable with resolving merge conflicts. Asks for review/merge of their pull requests from teammates. Is comfortable editing code based on review feedback from a pull request and resubmitting the branch code.

## DESIGN

## Comp Recreation

* Proficient  Developer captures the spirit and design intent of the comp. Some small details need polish to achieve a pixel-perfect match to the comp, but developer is clearly mindful of details and has made a conscious and careful effort to match the comp. Any design decisions left open to interpretation are handled thoughtfully and are well executed, but are more noticeable and/or unintuitive than they would be if the designer had provided the solution, or may not be totally seamless during screen-size transitions.
* Exceptional Developer skillfully captures the spirit and design intent of all comp details. Execution is pixel-perfect and any design decisions left open to interpretation are solved intentionally, are as seamless as if the designer had provided the solution, are handled gracefully, and enhance the overall design.

## PAIRING

## Collaboration

* Proficient  Can diplomatically handle issues that arise between the pair through respectful, focused, targeted feedback and implement changes to positively adapt the working relationship and keep the project on track. Can effectively implement tactics to support their partner’s learning and project goals, while also honoring their own personal learning and project goals, should the two be different or at different levels due to skill delta.
