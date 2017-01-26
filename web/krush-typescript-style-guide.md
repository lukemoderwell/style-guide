# Krush Typescript Style Guide

Adapted from [Microsoft's Typescript Style Guide](https://github.com/Microsoft/TypeScript/wiki/Coding-guidelines)

## Names

1. Use PascalCase for type names.
2. Do not use "I" as a prefix for interface names.
3. Use PascalCase for enum values.
4. Use camelCase for function names.
5. Use camelCase for property names and local variables.
6. Do not use "_" as a prefix for private properties.
7. Use whole words in names when possible.

## Types
1. Do not export types/functions unless you need to share it across multiple components.
2. Do not introduce new types/values to the global namespace.
3. Shared types should be defined in 'types.ts'.
4. Within a file, type definitions should come first.

## `null` and `undefined`
1. Use **undefined**, do not use null.
1. Exception: sometimes null is expected or produced by external/3p code.

## Comments
1. Use JSDoc style comments for functions, interfaces, enums, and classes.

## Strings
1. Use single quotes for strings unless content includes single quotes but no double quotes.
2. All strings visible to the user need to be localized (method to be determined).

## Style

1. Use arrow functions over anonymous function expressions.
2. Only surround arrow function parameters when necessary. <br />For example, `(x) => x + x` is wrong but the following are correct:
  1. `x => x + x`
  2. `(x,y) => x + y`
  3. `<T>(x: T, y: T) => x === y`
3. Always surround loop and conditional bodies with curly braces.
4. Open curly braces always go on the same line as whatever necessitates them.
5. Parenthesized constructs should have no surrounding whitespace. <br />A single space follows commas, colons, and semicolons in those constructs. For example:
  1. `for (var i = 0, n = str.length; i < 10; i++) { }`
  2. `if (x < 10) { }`
  3. `function f(x: number, y: string): void { }`
6. Use a single declaration per variable statement <br />(i.e. use `var x = 1; var y = 2;` over `var x = 1, y = 2;`).
7. `else` goes on the same line as the closing curly brace.
8. Use 4 spaces per indentation.
