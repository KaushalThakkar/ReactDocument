# ES6 ( ECMAScript)

1. Let & Const
2. Arrow function
3. Exports & Imports
4. Classes
5. Spread & Rest Opreators
6. Destructuring
7. Array function

# 1. Let & Const

- `let` is to say **new var**. You use it for variable value.

- `const`, if you plan on **creating a constant value**, so something which you only assigne once and **never change.**

- **In this course you will never see `var`, you will onliy see `let` and `const` and mostly it's `const`.**

## Example

###### Nromal
>JS
```js
var myname = 'Kaushal';
console.log(myname);

myname = 'Jack';
console.log(myname);
```
>Output (In Console)
```
Kaushal

Jack
```

###### With `let`
>JS
```js
let myname = 'Kaushal';
console.log(myname);

myname = 'Jack';
console.log(myname);
```
>Output (In Console)
```
Kaushal

Jack
```
- **Note :** You can not give same `let` name like `var`.


###### With `const`
>JS
```js
const myname = 'Kaushal';
console.log(myname);

myname = 'Jack';
console.log(myname);
```
>Output (In Console)
```
Kaushal

!!! Error (TypeError: Assignment to constant variable.)
```