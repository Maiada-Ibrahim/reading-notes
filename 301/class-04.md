#  React and Forms
## What is a ‘Controlled Component’?
n HTML, form elements such as \<input>, \<textarea>, and \<select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().
## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
because the form  is Controlled Inputs
 since setState() automatically merges a partial state into the current state, we only needed to call it with the changed parts.
 
## How do we target what the user is entering if we have an event handler on an input field?
keeping track of the visited fields, and handling form submission, Formik is one of the popular choices. However, it is built on the same principles of controlled components and managing state 
## [check her to read more ](https://reactjs.org/docs/forms.html)
---------------------------
## Why would we use a ternary operator?
Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.
Rewrite the following statement using a ternary statement
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
  condition ? value if true : value if false

## [check her to read more ](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)
