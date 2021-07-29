## React and Forms
* What is a ‘Controlled Component’?
  
In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”.
  Then the React component that renders a form also controls what happens in that form on subsequent user input.
  An input form element whose value is controlled by React in this way is called a “controlled component”.
  
  * Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  
   we update the state with their responses as soon as they enter them.
  Since the value attribute is set on our form element, the displayed value will always be this.state.value, making the React state the source of truth.
  Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.
  
* How do we target what the user is entering if we have an event handler on an input field?
   you can keep a variable in your state indicating if the sidebar is open and change the value of that when the button is clicked. 
   You can then use this state variable to decide if the sidebar should be given the hidden class or not.
     
     ## Why would we use a ternary operator?

     Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.
       
       ## The Conditional (Ternary) Operator
First, we’ll take a look at the syntax of a typical if statement:

```
       
       if ( condition ) {
  value if true;
} else {
  value if false;
}
```
Now, the ternary operator:
```
condition ? value if true : value if false
  ```
Here’s what you need to know:
* The condition is what you’re actually testing. The result of your condition should be true or false or at least coerce to either boolean value.
* A ? separates our conditional from our true value. Anything between the ? and the : is what is executed if the condition evaluates to true.
* Finally a : colon. If your condition evaluates to false, any code after the colon is executed.
