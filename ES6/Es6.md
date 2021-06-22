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


# 3. Exports & Imports

![Imports   Export](https://user-images.githubusercontent.com/64890185/122013750-1abc9d80-cddc-11eb-9e2b-3474fc678892.png)

## Example

>Util.js
```javascript
const getName = (user) => {
  return user.name;
}
const getPhone = (user) => {
  return user.Phone;
}

const getAddress = (user) => {
  return  user.getAdddress();
}

export getName;
export getPhone;
export default getAddress;
```
- You can also write like this...
```javascript
export const getName = (user) => {
  return user.name;
}
export const getPhone = (user) => {
  return user.Phone;
}

export default const getAddress = (user) => {
  return  user.getAdddress();
}
```
>App.js
```javascript
import Kaushal from 'util'; // Will still points to the default export, regardless of reference name.
import {getName, getPhone} from 'util'; // Will points to getName and the name should be precise.
```


# 4. Classes

- Classes are essentially  (basically) blueprint for object.

- A class is created with the class keyword and a class can have both properties and methods.

![calss](https://user-images.githubusercontent.com/64890185/122250375-3b254e80-cee7-11eb-8e65-908d3fcb4719.png)

## Example

```javascript
class Person{
    constructor(){
        this.name = 'Jack';
    }
    printMyName(){
        console.log(this.name);
    }
}
con     st person = new Person();
person.printMyName();
```
>Output (In Console)
```javascript
Jack
```
- This is simple example of class.

- Let's show with inheritance. 

```javascript
class Human{
    constructor(){
        this.gender = "male";
    }
    printGender(){
        console.log(this.gender);
    }
}
class Person extends Human {
    constructor(){
        super();
        this.name = 'Jack';
        this.gender = 'female';
    }
    printMyName(){
        console.log(this.name);
    }
}

const person = new Person();
person.printMyName();
person.printGender();
```
>Output (In Console)
```
Jack
female
```

- But, this is simple Javascript. So, how to use class through next generation JS (ES6) syntax.

- Below is the example of class in next generation JS (ES6) syntax.

```javascript
class Human{
  
    gender='male';

    printGender = () => {
        console.log(this.gender);
    }
}

class Person extends Human{
    name = 'Jack';
    gender = 'female';

    printMyName = () => {
        console.log(this.name);
    }
}
const person = new Person();
person.printMyName();
person.printGender();

```
>Output (In Console)
```
Jack
female
```
- **No constructor, No super keyword, No this keyword. It's ES6 syntax for class.**


# 5. Spread & Rest Operators
 
 - Actually it's only operator three dots.  **`...`**

**Spread :** Used to split up array elements OR objects properties. Like this,

```
const newArray = [...oldArray,1,2]
const newObject = {...oldObject,newProps:5}
````

**Rest :** Used to merge a list of function arguments into an array. Like this,

```
function sortArgs(...args){
    return args.sort();
}
````

##Example

```js
const numbers = [1,2,3];
const newNumber = [...numbers, 4];

console.log(newNumbers);
```
>Output 

```
[1,2,3,4]
```
 - without spread opreters output is,

 ```
 [[1,2,3],4]   
 ```

 - Let's show one more Example
 ```js
const person = {
    name = 'Jack'
};

const newPerson = {
    ...person,
    age: 28
}
 ```

 >Output
```
 age : 28
 name : 'Jack'.
```

 - So, that is a spread Opretors.

 - Lets, show Rest operators example.
 ```js
 const test = (...xx) => {
     return xx.filter(xy => xy === 2);
 }
 console.log(test(1,2,3));
 ```
 >Output
 ```
 [2]
 ```

 - Let's see one more Example
```js
 const words = ['Sprtay','Limit', 'elite','exuberant','destrution','present'];
 const result = word.filter(word => )
 
 console.log(result);
 ```
 >Output
```
 ["exuberant","destrution","present"]
 ```

# 6. Destructuring

- Easily extract array Elements or object properties and store in variables,

- for...

## Array Destructuring

```js
[a,b] = ['Hello', 'Kaushal']
console.log(a)     // Hello
console.log(b)     // Kaushal
```

## Object Destructuring

```js
[a,b] = ['Hello', 'Kaushal']
console.log(a)     // Hello
console.log(b)     // Kaushal
```
###### Example

```js
const numbers = [1,2,3];
[num1, num2] = nmbers;

console.log(num1, num3);

// Output : 1 3
```
- Object Destructuring is not supported by jsbin.

# 7. Array function

```js
const numbers = [1,2,3];    // Normal array

const newarray = number.map(num) => {   // Map is a builtin Array method , all the returns a new array.

    return num *2;
}

console.log(numbers);
console.log(newarray);
```
>Output
```
[1,2,3]

[2,4,6]
```