#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?

* What excites or interests you about coding?

** I love the 'hands on' aspect of coding, that I get to build something. I love architecture and the idea of creating and building something that people use and will make their lives better.

* What is a recent technical challenge you experienced and how did you solve it?

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?

* Talk about your preferred development environment.

* Which version control systems are you familiar with?
** I use Git for version control. Version control records the changes you make to documents over time so you can revisit them later.

* Can you describe your workflow when you create a web page?
** 
* If you have 5 different stylesheets, how would you best integrate them into the site?
** compress them into one rather than using @import, which loads sequentially and causes slow page loading.
* Can you describe the difference between progressive enhancement and graceful degradation?
** Graceful degredation starts with the most recent technology

* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
** Loop through images in an array, use setTimeout.

* If you could master one technology this year, what would it be?

* Explain the importance of standards and standards bodies.
** WC3 is standards bodies
** Standards are important because if they make it easier for other people to follow your code and everyone to be on the same page.

## HTML Questions

* What does a `doctype` do?
** It tells the browser to render in the Standards Mode/compliant way, rather than Quirks Mode. It came about because of the "broken" rendering of old IE browsers.
http://stackoverflow.com/questions/1818587/what-is-the-functionality-of-doctype 

* What's the difference between HTML and XHTML?
** XHTML uses stricter syntax (XML) than HTML. Must have closing tags on all elements, be lowercased,   

* What are `data-` attributes good for?
** Data attributes are something that came about with HTML 5. It's a way we can store snippets of data. The data should not be displayed to users, it's a way to identify certain elements. 
They can also be stored to contain information that is constantly changing, like scores in a game.
https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes
http://webdesign.tutsplus.com/tutorials/all-you-need-to-know-about-the-html5-data-attribute--webdesign-9642

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
** "session cookies live as long as browser WINDOW is open (not tab in which they were set) BUT sessionStorage is nulled as soon as you close the tab" 
** localStorage stores data until it's removed with Javascript or the user clears their cache.
** sessionStorage stores the data until the tab is closed or the session ends. It doesn't delete when the page reloads though. Session data is more secure than local Storage or cookies. Cookies can be read by other people over wifi. 
** Cookies can store less data.
http://stackoverflow.com/questions/29960037/localstorage-vs-sessionstorage-vs-cookies
http://stackoverflow.com/questions/19867599/what-is-the-difference-between-localstorage-sessionstorage-session-and-cookies/19869560#19869560

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

COMMIT NOW

## CSS Questions

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* How do you optimize your webpages for print?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Explain some of the pros and cons for CSS animations versus JavaScript animations.

## JS Questions

* Explain event delegation
* Explain how `this` works in JavaScript
* Explain how prototypal inheritance works
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the User Agent string?
* Explain AJAX in as much detail as possible.
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
* What are params?
* How do I make a migration to add a column in Rails?
* What is CSRF? How does Rails protect an app against this?
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
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
