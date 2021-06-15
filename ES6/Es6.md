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


# 2. Arrow Function 

- That is a different syntax for creating JavaScript function.

- A normal Js function looks like this, `function fn(){____}` .

- Now arrow function looks like this, `const myfn = () => {_____}` .

## Example
###### Nromal
>JS
```js
function printname(name)
{
    console.log(name);
}
printname('Kaushal');
```
>Output (In Console)
```
Kaushal
```

###### With Arrow function
>JS
```js
const printname = (name) => {

    console.log(name);
}
printname('Kaushal');
```
>Output (In Console)
```
Kaushal
```

- Now the this keyword thing is somwthing you will see throughout call of the course.

```
const myname = name => {           // Without brecakets when only one arg.
    console.log(name);  
}
```

- That's only valid for **exactly one argument** though, not for more and for less.

```
const myname = () => {          // When No any Argument.
    console.log('Kaushal');
}
```
- If two or more arguments, that time using this syntax.
```
const myname = (name,age) => {           // Without brecakets when only one arg.
    console.log(name,age);  
}
myname('Jack',25);
```

- Now, run with using return function.
```
const multiply = (number) => {           //You also write Without brecakets.
    return number * 2;
}
console.log (multiply (2));
```

- In this case you write in **Singal line.**
```
const multiply = number => number * 2;

console.log (multiply (2));
```
- This is a very short version of writing this function.
