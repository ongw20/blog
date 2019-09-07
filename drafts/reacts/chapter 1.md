# React - Typescript

## TypeScript offers several benefits over JavaScript
- Coding errors can be caught in the development process earlier
- Static types allow tools to be built that improve the developer experience and productivity
- JavaScript features that aren't implemented in all the browsers yet can actually be used in an app that targets those browsers

## Understanding basic types
#### Primitive types
- stirng
- number
- boolean
- undefined
- null
#### Any
TypeScript compiler gives a variable with no type annotation and no immediately assigned value, the `any` type. It is a way of opting out of type checking on a particular variable.
#### Void
`Void` is generally used to represent a non-returning function.
#### Never
`Never` represents something that would never occur and is typically used to specify unreachable areas of code.
#### Enumerations
`Enumerations` allow us to declare a meaningful set of friendly names that a variable can be set to.
#### Objects
`Object` type is shared with JavaScript and represents a non-primitive type. Objects can contain typed properties to hold bits of information.
#### Arrays
`Arrays` are structures that TypeScript inherits from JavaScript. We add type annotations to arrays as usual, but with square brackets at the end to denote that this is an array type.

## Creating interfaces, types aliases, and classes
#### Interfaces
`Interface` is a contract that defines a type with a collection of property and method definitions without any implementation.
#### Type aliases
`Type alias` creates a new name for a type.
#### Classes

## Structuring code into modules
### Module formats
- Asynchronous Module Definition(AMD): This is commonly used in code targeted for the browser and uses a `define` function to define modules.
- CommonJS: This format is used in Node.js programs. It uses `module.exports` to define modules and `require` to define dependencies.
- Universal Module Definition(UMD): This can be used in both browser apps and Node.js programs.
- ES6: This is the native JavaScript module format and uses the `export` keyword to define modules and `import` to define dependencies.
