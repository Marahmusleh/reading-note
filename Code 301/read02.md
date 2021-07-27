# React: Component Lifecycle Events

**What are component lifecycle events?**
React lets you define components as classes or functions. The methods that you are able to use on these are called lifecycle events.
These methods can be called during the lifecycle of a component, and they allow you to update the UI and application states.

![img](https://miro.medium.com/max/2000/0*0saPKFiTUk6W3FYp)


# componentDidMount()
This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions. 
If you do that, don’t forget to unsubscribe in componentWillUnmount().

  
## State and Props
What are props? Props is short for properties and they are used to pass data between React components. React’s data flow between components is uni-directional (from parent to child only).

How do you pass data with props? Here is an example of how data can be passed by using props:



class ParentComponent extends Component {
render() {
return (

);
} }

const ChildComponent = (props) => {
return

{props.name}

; }; Firstly, we need to define/get some data from the parent component and assign it to a child component’s “prop” attribute.
“Name” is a defined prop here and contains text data. Then we can pass data with props like we’re giving an argument to a function:
const ChildComponent = (props) => {
// statements }; And finally, we use dot notation to access the prop data and render it:

return

{props.name}

;
