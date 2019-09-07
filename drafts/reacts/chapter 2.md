# What is New in TypeScript 3

## Tuples
A `tuple` is like an array but the number of elements are fixed. It's a simple way to structure data and use some type safety. Tuples have had a few enhancements in TypeScript 3, so that they can be used with the popular `rest` and `spread` JavaScript syntax.

## The unknown type
`unknown` is a new type that has been added in TypeScript 3. Unknown types are type-checked. So, unknown can often be used as an alternative to `any`.

## Project references
TypeScript 3 allows TypeScript projects to depend on other TypeScript projects by allowing `tsconfig.json` to reference other `tsconfig.json` files.

## Default JSX properties
TypeScript 3 has also improved how we can set default properties on React components with `--strictNullChecks`. Before TypeScript 3, we had to set properties that had default values as optional and perform `null` checks when referencing them.
