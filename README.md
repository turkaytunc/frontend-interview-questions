# Interview Cheatsheet

## :pencil: Index

- [Normal Bir HTML Rendering Akisi](#Normal-Bir-HTML-Rendering-Akisi)
- [React Component Lifecycle](#React-Component-Lifecycle)
- [What is a Closure](#What-is-a-Closure)
- [Difference Between Class and Prototypal Inheritance](#Difference-Between-Class-and-Prototypal-Inheritance)
- [Mixin](#Mixin)
- [What is a Pure Function](#What-is-a-Pure-Function)

## Normal Bir HTML Rendering Akisi

1. HTML parse edilerek DOM ağacı oluşturulur,
2. JS ile DOM API gelen değişiklikler DOM Ağacını günceller
3. StyleSheet CSS tarafından parse edilir. StyleSheet kuralları oluşturulur
4. DOM Tree ve Style Rules birleştirilerek Render Tree oluşturulur.
5. Layout yani tarayıcının özellikleri (Dekstop, Mobile, Çözünürlük vb..) göre ekrana boyama işlemi gerçekleştirilir.

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

## Difference Between Class and Prototypal Inheritance

- Unlike most other languages, JavaScript’s object system is based on prototypes, not classes.
- Class Inheritance: A class is like a blueprint — a description of the object to be created. Classes inherit from classes and create subclass relationships: hierarchical class taxonomies.
- Instances are typically instantiated via constructor functions with the `new` keyword.

- Prototypal Inheritance: A prototype is a working object instance. Objects inherit directly from other objects.
- Instances may be composed from many different source objects, allowing for easy selective inheritance and a flat `[[Prototype]]` delegation hierarchy.
- Instances are typically instantiated via factory functions, object literals, or `Object.create()`.
- Concatenative inheritance: The process of inheriting features directly from one object to another by copying the source objects properties. In JavaScript, source prototypes are commonly referred to as mixins.

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
  sayBye() {
    alert(`Bye ${this.name}`);
  },
};

// usage:
class User {
  constructor(name) {
    this.name = name;
  }
}

// copy the methods
Object.assign(User.prototype, sayHiMixin);

// now User can say hi
new User('Dude').sayHi(); // Hello Dude!
```

## What is a Pure Function

- A function is a process which takes some input, called arguments, and produces some output called a return value.
- Pure function: Given the same input, will always return the same output.
- Pure function: Produces no side effects.
