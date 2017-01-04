#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?

* What excites or interests you about coding?

 * I love the 'hands on' aspect of coding, that I get to build something. I love architecture and the idea of creating and building something that people use and will make their lives better.

* What is a recent technical challenge you experienced and how did you solve it (demonstrate your resourcefulness and self-sufficiency)?
 * Coding challenge: tried different approaches, tested in Terminal
 * Issues with Ionic. Google it, stack overflow, forums, ask a fellow developer. 

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
 * Naming conventions -- do the function names make sense?
 * Are there clear comments to help future devs who work on the code?
 * Has the auth been tested for holes? Has the code been tested at all?
 * What's the user story (UI)?
 * How many clicks does it take for the user to accomplish their goal?
 * What is the runtime and runspace? How many resources/memory and time does it take to process?

* Talk about your preferred development environment.
 * Apple, Sublime, have terminal windows open to catch errors, Chrome developer tools

* Which version control systems are you familiar with? (READ UP ON GIT VS SVN)
 * I use Git for version control. Version control records the changes you make to documents over time so you can revisit them later. (TALK ABOUT HOW YOU'VE USED IT) I've used it in group projects, hackathons, and individually. I try to make commits every day.


* Can you describe your workflow when you create a web page?
 * Create a plan, figure out which technologies to use, set up a git repo, open up sublime, create basic html, set up routes and database if necessary, work on the core functionality, then styling, and testing.


* If you have 5 different stylesheets, how would you best integrate them into the site?
 * If all the stylesheets are needed on all the pages, compress them into one rather than using @import, which loads sequentially and causes slow page loading. Or just include the stylesheet on the view that's needed.

* Can you describe the difference between progressive enhancement and graceful degradation?
 * How your app works on newer/older browsers. What's the baseline? Different approaches.
 * Graceful degredation starts with the most recent technology

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
 * Loop through images in an array, use setTimeout.

* If you could master one technology this year, what would it be?
 * React / React Native

* Explain the importance of standards and standards bodies.
 * WC3 is standards bodies
 * Standards are important because if they make it easier for other people to follow your code and everyone to be on the same page.
 * A set of guidelines that everyone can adhere to

## HTML Questions

* What does a `doctype` do?
 * It tells the browser to render in the Standards Mode/compliant way, rather than Quirks Mode. It came about because of the "broken" rendering of old IE browsers.
http://stackoverflow.com/questions/1818587/what-is-the-functionality-of-doctype 

* What's the difference between HTML and XHTML?
 * XHTML uses stricter syntax (XML) than HTML. Must have closing tags on all elements, be lowercased, etc.  

* What are `data-` attributes good for?
 * Data attributes are something that came about with HTML 5. It's a way we can store snippets of data. The data should not be displayed to users, it's a way to identify certain elements. 
 * They can also be stored to contain information that is constantly changing, like scores in a game.
 https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes
 http://webdesign.tutsplus.com/tutorials/all-you-need-to-know-about-the-html5-data-attribute--webdesign-9642

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
 * "session cookies live as long as browser WINDOW is open (not tab in which they were set) BUT sessionStorage is nulled as soon as you close the tab" 
 * localStorage stores data until it's removed with Javascript or the user clears their cache.
 * sessionStorage stores the data until the tab is closed or the session ends. It doesn't delete when the page reloads though. Session data is more secure than local Storage or cookies. Cookies can be read by other people over wifi. 
 * Cookies can store less data.
 * Cookies are often used for login data (sent to the server?)
http://stackoverflow.com/questions/29960037/localstorage-vs-sessionstorage-vs-cookies
http://stackoverflow.com/questions/19867599/what-is-the-difference-between-localstorage-sessionstorage-session-and-cookies/19869560#19869560

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
 * CSS needs to be loaded first. Having the script tags at the bottom allows the page (document) to load first. This provides a better user experience because otherwise the page will stop to load the scripts. The other option, which is newer and IMO better, is to put the scripts in the head, under the css links and to put 'async' or 'defer' in the script tag. These allow the page to load while also fetching the script at the same time. With async, the script is loaded as soon as it's downloaded. Whichever script finishes first, will start first. If you need scripts to run in order, you use defer. Additionally, defer scripts start once the page fully loads. Async and defer may not run properly in IE <= 9 though. Don't use async and defer when using Angular though. 

## CSS Questions

* What is the difference between classes and IDs in CSS?
 * IDs are used once. Classes are used multiple times.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
 * resetting removes all of the default styling from the browser. Normalize is a base stylesheet, which styles the default elements to be consistent across browsers. 

* Describe Floats and how they work.
 * Take an element out of the normal flow of the page. Sticks it to the left/right and wraps the other elements (like text) around it.

* Describe z-index and how stacking context is formed.
 * The order of elements. Bigger numbers cover smaller numbers.
WHAT IS STACKING CONTEXT?

* Have you ever used a grid system, and if so, what do you prefer?
 * Bootstrap/Materialize has 12 columns (that's a grid system)

* Have you used or implemented media queries or mobile specific layouts/CSS?
 * Yes, I've used @media queries for responsive design.

* How do you optimize your webpages for print?
 *

* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
    * Adds more functionality, which also adds more complexity. Can confuse team members who are familiar with CSS but not preprocessors. May not be ideal if lots of different people will be editing CSS.
    * SASS, LESS, and Stylus are popular preprocessors. 
    * Variables, nesting, mixins, extend, color operations, if/else, loops, math, import other scss files.

* How would you implement a web design comp that uses non-standard fonts?
 * If a computer doesn't have the font locally, the browser selects an alternative fontd.
 * Universal fonts: Arial, Times New Roman, Courier New, Georgia, Verdanad
 * Use Google web fonts and link to them in the HTML header.
 * @font-face
 * Font.com
 * TypeKit

* Explain how a browser determines what elements match a CSS selector.
 * Browsers read from right to left, which is faster than left to right. There are likely less options for the browser to look through.
 * It's recommended to not use more than 2 selectors for a rule, because it takes the browser too much time.

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
 * All HTML elements can be considered boxes. In the box is content, padding, border, margin, in that order. 
 * When setting width and height, that only applies to the content section of the box. If you add padding, border, or margin, the box's width will be larger. You must keep this in mind when designing a page with a specific page width. All the images need to fit!

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
 * Normally (as mentioned above), height and width only contain the content. with border-box, the height and width also include padding and border, but not margin. 
 * This is like IE's old 'quirks mode'.
 * It's very effective for responsive design!
 * https://css-tricks.com/box-sizing/

* List as many values for the display property that you can remember.
 * Block, inline, none
 ```* none | inline | block | list-item | inline-list-item | inline-block | inline-table | table | table-cell | table-column | table-column-group | table-footer-group | table-header-group | table-row | table-row-group | flex | inline-flex | grid | inline-grid | run-in | ruby | ruby-base | ruby-text | ruby-base-container | ruby-text-container | contents``` 

* What's the difference between inline and inline-block?
 * display: inline doesn't break the flow of text. It accepts margin and padding but NOT height or width. Inline-block does.

* What's the difference between a relative, fixed, absolute and statically positioned element?
 * static: elements are static by default. Sticks to normal page flow. Using 'top', 'bottom', 'left', 'right', won't work.
 * relative: same as static, but top/left/right/bottom work.
 * absolute: removed from the flow of the document. Other elements act like it's not there. top/bottom/left/right work
 * fixed: removed from flow of document. However, they are relative to the document, not a parent. Unaffected by scrolling. <-- This is good for footers.
 * inherit: This causes the element to inherit the positioning value of its parent.

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
 * When two styles overlap, the bottom style has priority
 * !important, style (inline), IDs, classes, elements
 * Knowing specificity reduces unwanted formatting problems and can speed up your code.

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
 * Bootstrap and Materialize
 * I would make them easier to override, especially Materialize's colors.

* Have you played around with the new CSS Flexbox or Grid specs?
 * A little.
 * https://css-tricks.com/snippets/css/a-guide-to-flexbox/
 * https://github.com/kristoferjoseph/flexboxgrid
 * https://css-tricks.com/snippets/css/complete-guide-grid/

* Have you ever worked with retina graphics? If so, when and what techniques did you use?
 * I haven't used it but I've read up on different techniques.

* Explain some of the pros and cons for CSS animations versus JavaScript animations.
 * CSS is good for small, self-contained states for UI elements like pop-out nav menus and tooltips.
 * Javascript is better when you need more control and functionality. There are many frameworks. jQuery has an animate() method that I've used before. 
 * https://developers.google.com/web/fundamentals/design-and-ui/animations/css-vs-javascript

## JS Questions

* Explain event delegation
 * Event delegation allows you to target a parent element, instead of adding an event listener to many individual objects. For example, you can add a click event listener to a <ul> element instead of each individual <li> element.
 * Reference: https://davidwalsh.name/event-delegate

* Explain how `this` works in JavaScript
* Explain how prototypal inheritance works
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
** 

* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
  * How would you go about checking for any of these states?

* What is a closure, and how/why would you use one?

* What's a typical use case for anonymous functions?
** AJAX. Or if you only need to execute a block of code once and you don't need to call it again (self-invoking)
** (function() {
  console.log('called');
})();

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
** defining a function 
** callinga function and setting it's return fuction to a variable
** creatinga new object and assigning it to a variable


* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the User Agent string?
* Explain AJAX in as much detail as possible.
** asynchronous javascipt call. 
** we use it for http requests, api requests
** get or send info without reloading the page
** you can set up an event listener, on a form for example, to send the data without reloading the page.
** AJAX request to a server (yours or somewhere else). You have to get something back, whether its data or an error.

* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
** Event bubbling happens when there are nested items and you make a change to one of the items and the change is applied to all the events above it (the parents). It propagates up the DOM tree. A great example of this: https://codepen.io/fightingtheboss/pen/BNajOr 

* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What tools and techniques do you use debugging Javascript code?
* What language constructions do you use for iterating over object properties and array items?

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
* What is the difference between a symbol and a string?
* What is the difference between a class method and an instance method?
* What is the difference between local variables, instance variables, and class variables?
* What is a range?
* In ruby, what does attr_accessor do?  
* What is the purpose of environment files under the config folder in Rails? (development, test, production)
* What is the purpose of the application.rb file in Rails?
* How can you define a constant?
* What is the purpose of `yield`?
* How do you store API keys when creating an app?
* How do I send parameters through a url?
* Explain MVC
* What is a `before_action`? When would you use it?
* What do controllers do in rails?
* What is RESTful routing?
* What is a polymorphic association?
** something that belongs to more than one database model (2:1)???

* What are params?
* How do I make a migration to add a column in Rails?
* What is CSRF? How does Rails protect an app against this?
** CSRF is when someone tries to... hack you're site? Mess with your page...? Rails prevents access to certain protocols. 
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
** Catch bugs
** It takes more time

* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?
