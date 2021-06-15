# What is React?

- React is one of the most popular and widely used **Libraries** (it's **Not** a **Framework**) for frontens development. To give you a gentle  introduction. 

- React is an open sources js library used for fronted developement, which was developed by Jordan Walke a software Egineer at facebook.

- "A Javascropt library for buildinguser Interface".

- React app is run on the browser(client side), Don't run on the server.

- React is all about of using **Components** for building.

- Like this,

![Components](https://user-images.githubusercontent.com/64890185/121854756-32c6eb00-cd10-11eb-8348-743422febaf7.png)

- React components can we call of Custom HTML elements.
 
# Why use Reacet Js?

- The coew objective of React JS is providing the bast possible rendering performance.

- It's strength comes form the focus on **Individul Components.**

- In stead of working on the entire web app ReactJS allows a developer to brack down the comlex UI into simpler components.

- Reactjs is definitely good for the web development and give better performance then all other JS language like Angular, Vue.js, Ember etc.

- Reactjs used a special syntax called **JSX** which makes writing js easier.

- **Reactjs is focus on logic.**

- **9699** companies reportedly use **React** in their tech stacks, including **Uber, Netflix,** and **Facebook.**
![WhoUseReact](https://user-images.githubusercontent.com/64890185/121889035-543acd80-cd36-11eb-99e0-3fc42a69e19e.png)

# How to use React Js?

## Simple Program (without React)

>**HTML**
```html
<div class="person">
  <h1>Kaushal</h1>
  <p>Your age : 25</p>
</div>

<div class="person">
  <h1>Jack</h1>
  <p>Your age : 28</p>
</div>
```
>**CSS**
```css
.person{
  display: inline-block;
  margin: 10px;
  border: 1px solid #eee;
  box-shadow: 0 2px 2px #ccc;
  width: 200px;
  padding: 20px;
}
```
>OUTPUT

![WithoutReactOutput](https://user-images.githubusercontent.com/64890185/121868746-f9e24280-cd1e-11eb-9b28-9261e81447a4.png)

## With React

>**HTML**
```html
<div id="p1"></div>

<div class="person">
  <h1>Jack</h1>
  <p>Your age : 28</p>
</div>
```
>**CSS**
```css
.person{
  display: inline-block;
  margin: 10px;
  border: 1px solid #eee;
  box-shadow: 0 2px 2px #ccc;
  width: 200px;
  padding: 20px;
}
```
>**JS** (Add react 16.0.1, reactDOM 16.0.1 & Bable Preprocessor)
```js
function Person(){
  return( 
    <div class="person">
      <h1>Kaushal</h1>
      <p>Your Age: 25</p>
    </div>
  );
}

ReactDOM.render(<Person/>, document.querySelector("#p1"));
```
- **But , here 2 or more "Div" teg so, using props let see...**

>**HTML**
```html
<div id="p1"></div>

<div id="p2"></div>
```
>**JS** (Add react 16.0.1, reactDOM 16.0.1 & Bable Preprocessor)
```js
function Person(props){
  return( 
    <div class="person">
        <h1>{props.name}</h1>
        <p>{props.age}</p>
    </div>
  );
}

ReactDOM.render(<Person name="Kaushal" age="Your Age: 25"/>, document.querySelector("#p1"));
ReactDOM.render(<Person name="Jack" age="Your Age: 28"/>, document.querySelector("#p2"));
```
- **Here using 2 "Div" tags on html page. so, how to create in singal "Div" tag. Lets, see...**

 >**HTML**
```html
<div id="app"></div>
```
>**JS** (Add react 16.0.1, reactDOM 16.0.1 & Bable Preprocessor)
```js
function Person(props){
  return( <div class="person">
      <h1>{props.name}</h1>
      <p>{props.age}</p>
    </div>
  );
}
var App = (
  <div>
    <Person name="Kaushal" age="Your Age: 25"/>
    <Person name="Jack" age="Your Age: 28"/>
  </div>
);

ReactDOM.render(App, document.querySelector("#app"));
```
>OUTPUT

![WithoutReactOutput](https://user-images.githubusercontent.com/64890185/121868746-f9e24280-cd1e-11eb-9b28-9261e81447a4.png)


- **Now learn about a ES6 ( ECMAScript ).**