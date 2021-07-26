### React
React is an open-source, front end, JavaScript JavaScript library created by Facebook. React is a User Interface (UI) library. React is a tool for building UI components.


### What is React?
React only for the application’s view layer. The view layer of the Model View Controller (MVC) architecture is in charge of how the app looks and sounds.


### Why React?
Because of React's fast design of complex apps, improved usability, reusable modules, unidirectional data flow, small learning curve, and dedicated tools for quick debugging, its success has surpassed that of any other front-end development frameworks.


### Hello World in React
The smallest React example looks like this:
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

### JavaScript Syntax Extension (JSX)
JSX is a JavaScript syntax extension. It's a term that's used in React to explain how the user interface might appear. We can write HTML structures in the same file as JavaScript code by using JSX. Since complicated JavaScript DOM constructs are avoided, the code is simpler to grasp and debug.

Normal DOM

index.html
```
<!DOCTYPE html>
<html>
  <body>

    <p id="demo"></p>
    <script src="./js/app.js"></script>
  </body>
</html> 
```
app.js
```
const dom = document.getElementById('demo');

let textDOM = document.createElement(`p`);
textDOM.textContent = 'text From JS File use DOM';
dom.appendChild(textDOM);
JSX DOM
```

index.html
```
<!DOCTYPE html>
<html>
  <body>

    <p id="root"></p>
  </body>
</html> 
index.js

ReactDOM.render(
  <h1>text From React File use JSX</h1>,
  document.getElementById('root')
);
```
