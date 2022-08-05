# Variables (biến)

## I. Declaration of variables (khai báo biến)

1. Declare a variable (khai báo biến)

- Keyword to declare a variable: `var, let, const`

```js
var a = 1;
let b = 2;
const c = 3;
```

2. Rules for naming variables

- Variable name must start with a letter or underscore

```js
var _name = "John Doe"; // valid
```

- Variable name can contain letters, numbers, and underscores

```js
var name = "John Doe"; // valid
```

- Variable name cannot start with a number

```js
var 1name = 'John Doe'; // invalid
```

- Variable name cannot contain a space, hyphen, or dot, or any other special character

```js
var name-name = 'John Doe'; // invalid
var name.name = 'John Doe'; // invalid
var name/name = 'John Doe'; // invalid
var name*name = 'John Doe'; // invalid
```

- Variable name cannot contain a reserved keyword

```js
var var = 'John Doe'; // invalid
```

<!-- Note -->

**_Note_**: Reserved keywords are: `var, let, const, if, else, ...`

## II. Type of variables (kiểu biến)

- Type of variables is determined by the value of the variable

```js
var a = 1; // type: number
var b = "1"; // type: string
var c = true; // type: boolean
var d = null; // type: object
var e = undefined; // type: undefined
var f = {}; // type: object
var g = []; // type: array
```

## III. Scope (phạm vi)

- Scope is the area of a program where variables can be defined and used

### 1. Global scope (phạm vi toàn cục)

- Global scope is the area of a program where variables can be defined and used

```js
var a = 1; // global scope
function myFunction() {
  var b = 2; // local scope
  console.log(a); // 1
}
console.log(a); // 1
console.log(b); // ReferenceError: b is not defined
```

### 2. Local scope (phạm vi nội bộ)

- Local scope is the area of a function where variables can be defined and used

```js
function myFunction() {
  var a = 1; // local scope
  console.log(a); // 1
}
console.log(a); // ReferenceError: a is not defined
```

## IV. Hoisting

- Hoisting is the process of moving all variable declarations to the top of a function

```js
a = 1;
var a; // hoisting
console.log(a); // 1
```

- Hoisting is not applicable to `const` and `let`

```js
a = 1;
const a; // will throw an error
b = 2;
let b; // will throw an error
```
