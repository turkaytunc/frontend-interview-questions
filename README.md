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
