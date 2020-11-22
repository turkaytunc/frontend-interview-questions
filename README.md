# Interview Cheatsheet

## :pencil: Index

- [Normal Bir HTML Rendering Akisi](#Normal-Bir-HTML-Rendering-Akisi)
- [React Component Lifecycle](#React-Component-Lifecycle)
- [What is a Closure](#What-is-a-Closure)
- [Difference Between Class and Prototypal Inheritance](#Difference-Between-Class-and-Prototypal-Inheritance)

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
