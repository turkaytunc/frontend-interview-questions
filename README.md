# :pencil: Frontend Interview Questions

## Table of Contents

- [What are variables](#What-are-variables)
- [What are constants](#What-are-constants)
- [What is array](#What-is-array)
- [Why we need software testing](#Why-we-need-software-testing)
- [What is program execution](#What-is-program-execution)
- [How Rendering Works Step by Step](#How-Rendering-Works-Step-by-Step)
- [React Component Lifecycle](#React-Component-Lifecycle)
- [What is a Closure](#What-is-a-Closure)
- [Difference Between Class and Prototypal Inheritance](#Difference-Between-Class-and-Prototypal-Inheritance)
- [What is Mixin](#Mixin)
- [What is a Pure Function](#What-is-a-Pure-Function)
- [Function Composition](#Function-Composition)
- [Functional Programming](#Functional-Programming)
- [What is a Promise](#What-is-a-Promise)
- [What is Higher Order Component](#Higher-Order-Component)
- [What does setState do](#What-does-setState-do)
- [What is the difference between state and props](#What-is-the-difference-between-state-and-props)
- [What is react element](#What-is-react-element)
- [What is JSX](#What-is-JSX)
- [How to bind methods or event handlers](#How-to-bind-methods-or-event-handlers)
- [What is key prop](#What-is-key-prop)
- [What is ref and useRef](#What-is-ref-and-useRef)
- [What is Virtual DOM](#What-is-Virtual-DOM)
- [What is context](#What-is-context)
- [What is react children](#What-is-react-children)
- [What is super constructor](#What-is-super-constructor)
- [What is Reconciliation](#What-is-Reconciliation)
- [What is react fragments](#What-is-react-fragments)
- [What is an algorithm](#What-is-an-algorithm)
- [What is a compiler and how it works](#What-is-a-compiler-and-how-it-works)
- [What is DRY principle](#What-is-DRY-principle)
- [What is FIFO](#What-is-FIFO)
- [What is LIFO](#What-is-LIFO)
- [Linear vs non-linear data structures](#Linear-vs-non-linear-data-structures)
- [What is react portal](#What-is-react-portal)
- [What is Currying](#What-is-Currying)
- [What is SPA](#What-is-SPA)
- [What Is Server-Side Rendering](#What-Is-Server-Side-Rendering)
- [What is the difference between undefined and null](#What-is-the-difference-between-undefined-and-null)
- [What is event loop](#What-is-event-loop)
- [What is DOM](#What-is-DOM)
- [What is event bubbling](#What-is-event-bubbling)
- [What is event capturing](#What-is-event-capturing)
- [Explain stopPropagation method](#Explain-stopPropagation-method)
- [Explain preventDefault method](#Explain-preventDefault-method)
- [How to evaluate multiple expressions in one line](#How-to-evaluate-multiple-expressions-in-one-line)
- [What is object prototype](#What-is-object-prototype)
- [What is hoisting](#What-is-hoisting)
- [What is IIFE](#What-is-IIFE)
- [What is functor](#What-is-functor)
- [Explain the difference between call bind apply](#Explain-the-difference-between-call-bind-apply)
- [What are Higher Order Functions](#What-are-Higher-Order-Functions)
- [What is a Callback function](#What-is-a-Callback-function)
- [What is REST](#What-is-REST)

## What are variables

- Variables are used for storing the input of a program or can be computational results during program execution.

## What are constants

- A constant is a programming entity whose value can’t be changed or modified during program execution.

## What is array

- An array is a data structure that contains a group of elements.
- Typically these elements are all of the same data type, such as an integer or string.

[:arrow_up: Back to Top](#Table-of-Contents)

## Why we need software testing

- Some mistakes are minor but some can be very expensive or dangerous.
- We need to constantly check and test our software to make sure that no gaps exist.
- It makes the software more reliable and easy to use.
- Thoroughly tested software ensures reliable and high-performance software operation.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is program execution

- Program execution is the process that a computer executes the instructions of a computer program.

[:arrow_up: Back to Top](#Table-of-Contents)

## How Rendering Works Step by Step

1. Parsing HTML and creating DOM tree.
2. DOM tree updates using javascript based on DOM API
3. Parsing CSS. Create StyleSheet rules.
4. DOM Tree and Style Rules combine together and creates Render Tree.
5. Render layout based on device(Mobile, Desktop).

[:arrow_up: Back to Top](#Table-of-Contents)

## React Component Lifecycle

1. Mounting
   - constructor()
   - static getDerivedStateFromProps()
   - render()
   - componentDidMount()
2. Updating
   - static getDerivedStateFromProps()
   - shouldComponentUpdate()
   - render()
   - getSnapshotBeforeUpdate()
   - componentDidUpdate()
3. Unmounting
   - componentWillUnmount()
4. Error Handling
   - static getDerivedStateFromError()
   - componentDidCatch()

## What is a Closure

- A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment).
- In other words, a closure gives you access to an outer function’s scope from an inner function.
- In JavaScript, closures are created every time a function is created, at function creation time.

[:arrow_up: Back to Top](#Table-of-Contents)

## Difference Between Class and Prototypal Inheritance

- Unlike most other languages, JavaScript’s object system is based on prototypes, not classes.
- Class Inheritance: A class is like a blueprint — a description of the object to be created. Classes inherit from classes and create subclass relationships: hierarchical class taxonomies.
- Instances are typically instantiated via constructor functions with the `new` keyword.

- Prototypal Inheritance: A prototype is a working object instance. Objects inherit directly from other objects.
- Instances may be composed from many different source objects, allowing for easy selective inheritance and a flat `[[Prototype]]` delegation hierarchy.
- Instances are typically instantiated via factory functions, object literals, or `Object.create()`.
- Concatenative inheritance: The process of inheriting features directly from one object to another by copying the source objects properties. In JavaScript, source prototypes are commonly referred to as mixins.

[:arrow_up: Back to Top](#Table-of-Contents)

## Mixin

- Mixin is a class containing methods that can be used by other classes without a need to inherit from it.
- In other words, a mixin provides methods that implement a certain behavior, but we do not use it alone, we use it to add the behavior to other classes.

- Example

```js
// mixin
let sayHiMixin = {
  sayHi() {
    alert(`Hello ${this.name}`);
  },
};

// create user
class User {
  constructor(name) {
    this.name = name;
  }
}

// copy the methods
Object.assign(User.prototype, sayHiMixin);

// now User can say hi
new User('Turkay').sayHi(); // Hello Turkay!
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is a Pure Function

- A function is a process which takes some input, called arguments, and produces some output called a return value.
- Pure function: Given the same input, will always return the same output.
- Pure function: Produces no side effects.

[:arrow_up: Back to Top](#Table-of-Contents)

## Function Composition

- Function composition is the process of combining two or more functions to produce a new function. Composing functions together is like snapping together a series of pipes for our data to flow through.

[:arrow_up: Back to Top](#Table-of-Contents)

## Functional Programming

- Functional programming is a programming paradigm, meaning that it is a way of thinking about software construction based on some fundamental, defining principles.

- Functional programming is the process of building software by composing pure functions and avoiding shared state, mutable data, and side-effects.

- Functional programming is declarative rather than imperative, and application state flows through pure functions.

- Contrast with object oriented programming, where application state is usually shared and colocated with methods in objects.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is a Promise

- A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved.
- A promise may be in one of 3 possible states: fulfilled, rejected, or pending.
- Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.

- Promises following the spec must follow a specific set of rules:
  - A promise or “thenable” is an object that supplies a standard-compliant .then() method.
  - A pending promise may transition into a fulfilled or rejected state.
  - A fulfilled or rejected promise is settled, and must not transition into any other state.
  - Once a promise is settled, it must have a value (which may be undefined). That value must not change.

[:arrow_up: Back to Top](#Table-of-Contents)

## Higher Order Component

- A higher-order component is just a function that takes an existing component and returns another component that wraps it.

[:arrow_up: Back to Top](#Table-of-Contents)

## What does setState do

- setState() schedules an update to a component’s state object. When state changes, the component responds by re-rendering.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is the difference between state and props

- Props get passed to the component (similar to function parameters) whereas state is managed within the component (similar to variables declared within a function).

[:arrow_up: Back to Top](#Table-of-Contents)

## What is react element

- An element is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. Elements can contain other elements in their props.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is JSX

- JSX stands for JavaScript XML.
- JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement() and/or appendChild() methods.
- JSX is an extension of the JavaScript language based on ES6, and is translated into regular JavaScript at runtime.

[:arrow_up: Back to Top](#Table-of-Contents)

## How to bind methods or event handlers

- In JavaScript classes, the methods are not bound by default. The same thing applies for React event handlers defined as class methods.

```js
class SomeButton extends React.Component {
  constructor(props) {
    super(props);
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    //some code
  }
}
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is key prop

- A “key” is a special string attribute you need to include when creating lists of elements.
- Keys help React identify which items have changed, are added, or are removed.
- The best way to pick a key is to use a string that uniquely identifies a list item among its siblings.

```js
const todoItems = todos.map((todo) => <li key={todo.id}>{todo.text}</li>);
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is ref and useRef

- Refs provide a way to access DOM nodes or React elements created in the render method.

```js
const refContainer = useRef(initialValue);
```

- useRef returns a mutable ref object whose .current property is initialized to the passed argument (initialValue). The returned object will persist for the full lifetime of the component.

```js
function TextInputWithFocusButton() {
  const inputEl = useRef(null);
  const onButtonClick = () => {
    // `current` points to the mounted text input element
    inputEl.current.focus();
  };
  return (
    <>
      <input ref={inputEl} type="text" />
      <button onClick={onButtonClick}>Focus the input</button>
    </>
  );
}
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is Virtual DOM

- When new elements are added to the UI, a virtual DOM, which is represented as a tree is created. Each element is a node on this tree.
- If the state of any of these elements changes, a new virtual DOM tree is created. This tree is then compared or “diffed” with the previous virtual DOM tree.
- Once this is done, the virtual DOM calculates the best possible method to make these changes to the real DOM. This ensures that there are minimal operations on the real DOM.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is the difference between Shadow DOM and Virtual DOM

- The Shadow DOM is a browser technology designed primarily for scoping variables and CSS in web components.
- The Virtual DOM is a concept implemented by libraries in JavaScript on top of browser APIs.
- Virtual DOM is creating a copy of the whole DOM object, and Shadow DOM creates small pieces of the DOM object which has their own, isolated scope for the element they represent.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is react fiber

- React Fiber is a set of internal algorithms for rendering graphics used by the JavaScript library React, as opposed to its old rendering algorithm, Stack.
- The actual syntax for programming with React does not change; only the way that the syntax is executed has changed.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is context

- Context provides a way to pass data through the component tree without having to pass props down manually at every level.

- In a typical React application, data is passed top-down (parent to child) via props, but this can be cumbersome for certain types of props that are required by many components within an application.

- Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is react children

- Children is a prop that allow you to pass components as data to other components

[:arrow_up: Back to Top](#Table-of-Contents)

## What is super constructor

- The super keyword is used to access and call functions on an object's parent.
- When used in a constructor, the super keyword appears alone and must be used before the this keyword is used.
- The super keyword can also be used to call functions on a parent object.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is Reconciliation

- Reconciliation is the process through which React updates the DOM.
- When a component’s state changes, React has to calculate if it is necessary to update the DOM.
- It does this by creating a virtual DOM and comparing it with the current DOM.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is react fragments

- A common pattern in React is for a component to return multiple elements.
- Fragments let you group a list of children without adding extra nodes to the DOM.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is an algorithm

- An algorithm can be defined as a set of finite steps that when followed helps in accomplishing a particular task.
- Important features of an algorithm are clarity, efficiency, and finiteness.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is a compiler and how it works

- A compiler is a computer program that translates written code in one programming language into another language.

- Compiler usually follows these steps:
  1. Lexical Analysis
  2. Syntax Analysis
  3. Semantic Analysis
  4. Intermediate Code Generation
  5. Code Optimization
  6. Code Generation

[:arrow_up: Back to Top](#Table-of-Contents)

## What is DRY principle

- DRY stands for Don’t Repeat Yourself.
- DRY is a principle of software development aimed at reducing repetition of software patterns.
- Violations of DRY are typically referred to as WET solutions, which is commonly taken to stand for "write every time", "write everything twice".

[:arrow_up: Back to Top](#Table-of-Contents)

## What is FIFO

- FIFO is an abbreviation for first in, first out.
- It is a method for handling data structures where the first element is processed first and the newest element is processed last.
- The data structure that implements FIFO is Queue.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is LIFO

- LIFO is an abbreviation for Last in, first out is same as fist in, last out (FILO).
- It is a method for handling data structures where the last element is processed first and the first element is processed last.
- The data structure that implements LIFO is Stack.

[:arrow_up: Back to Top](#Table-of-Contents)

## Linear vs non-linear data structures

- In linear data structure, data elements are sequentially connected and each element is traversable through a single run. Examples: Array, List, Queue, Stack.
- In non-linear data structure, data elements are hierarchically connected and are present at various levels. Examples: Graph, Tree.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is react portal

- Portal is used to render children into a DOM node that exists outside the DOM hierarchy of the parent component.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is Currying

- Currying is the technique of converting a function that takes multiple arguments into a sequence of functions that each take a single argument.

```js
const add = (a) => (b) => a + b;
const result = add(2)(3);
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is SPA

- A single-page application (SPA) is a web application or website that interacts with the user by dynamically rewriting the current web page with new data from the web server, instead of the default method of the browser loading entire new pages.
- The goal is faster transitions that make the website feel more like a native app.
- In a SPA, all necessary HTML, JavaScript, and CSS code is either retrieved by the browser with a single page load or the appropriate resources are dynamically loaded and added to the page as necessary.

[:arrow_up: Back to Top](#Table-of-Contents)

## What Is Server-Side Rendering

- Server-side rendering (SSR) is the process of rendering web pages on a server and passing them to the browser (client-side), instead of rendering them in the browser.
- The website loads quickly because the browser fetches content from the server before rendering it for the user.
- More API calls to the server are made, because they’re made per request.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is the difference between undefined and null

- Both are are falsy values.
- undefined is the default value of a variable that has not been assigned a specific value.
- null is a value that represents no value. null is value that has been explicitly defined to a variable.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is event loop

- JavaScript has a concurrency model based on an event loop, which is responsible for executing the code, collecting and processing events, and executing queued sub-tasks.
- A JavaScript runtime uses a message queue, which is a list of messages to be processed. Each message has an associated function which gets called in order to handle the message.
- The event loop’s purpose is to look at the call stack and the queue. When the stack is empty, it takes the first thing on the queue and executes it.
- A very interesting property of the event loop model is that JavaScript, unlike a lot of other languages, never blocks.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is DOM

- DOM stands for Document Object Model.
- When the browser first parses HTML document it creates a big object based on the HTML document this is the DOM.
- It is a tree structure that is created from HTML.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is event bubbling

- It relates to the order in which event handlers are called when one element is nested inside a second element, and both elements have registered a listener for the same event (a click, for example).
- In the bubbling phase, the event bubbles up or it goes to its parent until it reaches all the way to the window object.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is event capturing

- When an event occurs on a DOM element, that event does not entirely occur on that just one element.
- In Capturing Phase, the event starts from the window all the way down to the element that triggered the event.

[:arrow_up: Back to Top](#Table-of-Contents)

## Explain stopPropagation method

- The stopPropagation() method of the Event interface prevents further propagation of the current event in the capturing and bubbling phases.
- It does not, however, prevent any default behaviors from occurring; for instance, clicks on links are still processed.

[:arrow_up: Back to Top](#Table-of-Contents)

## Explain preventDefault method

- The Event interface's preventDefault() method tells the user agent that if the event does not get explicitly handled, its default action should not be taken as it normally would be.
- If used in a form element it prevents it from submitting. If used in an anchor element it prevents it from navigating. If used in a contextmenu it prevents it from showing or displaying.

[:arrow_up: Back to Top](#Table-of-Contents)

## How to evaluate multiple expressions in one line

- We can use the , or comma operator to evaluate multiple expressions in one line.
- It evaluates from left-to-right and returns the value of the last item on the right or the last operand.

```js
let variable = 5;

variable = (variable++, (variable *= 5), (variable -= 8), (variable += 3));
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is object prototype

- Prototypes are the mechanism by which JavaScript objects inherit features from one another.
- Objects can have a prototype object, which acts as a template object that it inherits methods and properties from.
- The prototype property can be used to add methods to existing constructors.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is hoisting

- In JavaScript, a variable can be declared after it has been used.
- A variable can be used before it has been declared.
- Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope.
- JavaScript only hoists declarations, not initializations.

```js
var x = 5; // Initialize x
var y; // Declare y
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is IIFE

- IIFE is stands for "Immediately Invoked Function Expression".
- IIFE is a JavaScript function that runs as soon as it is defined.
- The function becomes a function expression which is immediately executed.
- The variable within the expression can not be accessed from outside it.

```js
(function () {
  //statements
  //statements
  //statements
})();
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is functor

- A Functor is something that is Mappable or something that can be mapped between objects in a Category.
- A category can be a collection of objects, arrays, functions.

```js
[1, 2, 3].map((x) => x * 2); //=> [2, 4, 6]
```

[:arrow_up: Back to Top](#Table-of-Contents)

## Explain the difference between call bind apply

- They are all attach "this" into function (or object) and the difference is in the function invocation.
- Call/apply call the function immediately, whereas bind returns a function that, when later executed, will have the correct context set for calling the original function.
- This way you can maintain context in async callbacks and events.

```js
let person = {
  firstname: 'John',
  lastname: 'Doe',
  getFullName: function () {
    let fullname = this.firstname + ' ' + this.lastname;
    return fullname;
  },
};

let logName = function (lang1, lang2) {
  console.log('Logged: ' + this.getFullName());
  console.log('Arguments: ' + lang1 + ' ' + lang2);
  console.log('-----------');
};

let logPersonName = logName.bind(person); // Binding this keyword, returns function.
logPersonName('en');

logName.call(person, 'en', 'es'); // Binds this keyword to given object and calls function
logName.apply(person, ['en', 'es']); // Same as call but takes arguments as an array
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What are Higher Order Functions

- A higher order function is a function that takes a function as an argument, or returns a function.

[:arrow_up: Back to Top](#Table-of-Contents)

## What is a Callback function

- A Callback function is a function that is gonna get called at a later point in time.

```js
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```

[:arrow_up: Back to Top](#Table-of-Contents)

## What is REST

- REST is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems.
- 6 guiding constraints which must be satisfied if an interface needs to be referred as RESTful.

1. Client–server – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.  
2. Stateless – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.  
3. Cacheable – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.  
4. Uniform interface – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.  
5. Layered system – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot see beyond the immediate layer with which they are interacting.

[:arrow_up: Back to Top](#Table-of-Contents)
