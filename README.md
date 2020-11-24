# :pencil: Javascript-React Interview Cheatsheet

## Table of Contents

- [How Rendering Works Step by Step](#How-Rendering-Works-Step-by-Step)
- [React Component Lifecycle](#React-Component-Lifecycle)
- [What is a Closure](#What-is-a-Closure)
- [Difference Between Class and Prototypal Inheritance](#Difference-Between-Class-and-Prototypal-Inheritance)
- [Mixin](#Mixin)
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
