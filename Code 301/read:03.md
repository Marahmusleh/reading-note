## Passing Functions as Props

1-We use the array.map() to store new modified elements to a new array in order to use it for a different purpose.

2-To loop through an array and display each value we use the map() method within the inline curly brackets of JSX. An example of that using function based components:
```
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) => <li>{number}</li>);

  return <ul>{listItems}</ul>;
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById("root")
);
```

3-Each list item in ReactJs needs a unique key, which is an attribute that cant be passed as props to the child components and its value is usually a string.

4-The purpose of the keys is to give the list items a stable identity and to help React identifying which items have changed, added or removed.

## The Spread Operator
* The spread operator ...arr can be used to expand an iterable object such as arrays into a list of arguments, it can also be used to add or combine arrays or objects together.

Things that the spread operator can do :

* Expands iterable objects into lists of arguments for methods and functions.
* It can pass multiple iterables.
* It can merge arrays together.
* It copies arrays/objects without changing the original array/object.

## Passing Functions Between Components
* The first thing to do in order to pass a function to another component is to give the object an attribute with the method as its value to pass it as props.

* The increment method increases the counter of the person name whenever the button is clicked.

* We pass methods from a parent to a child component using props.

* The child component can invoke the method by calling it and passing arguments inside it.
