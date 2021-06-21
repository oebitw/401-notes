# Component Composition

## Review, Research, and Discussion

1) Can a parent component access the state of a child component?

yes, we can access the child's state using Refs. we will assign a Refs for the child component in the parent component. then using Refs we can access the child's state.


2) What can be passed along in a prop variable?

Any information, function, JavaScript that needs to be passed down.


3) How can a child component “know” the state of another component?

- component props: What we pass from the parent component to the child component to can access them.

- component state: Its a object specific to the one components.

- application state: Represent all the state of the application.

## Vocabulary Terms

1) component props

Keyword in React for properties, can be any information, function, JavaScript that needs to be passed to another component. Can only be passed in one direction, from the root to its children, no way for data to be passed up.

2) component state

React components have built in state object, which is where you story property values that belong to the component. When the state object changes, t he component re-renders.

3) application state

 In an application, state is interface between data (from backend or local change) and the representation of this data with UI elements on the front-end. State is able to keep the data of different components in sync because each state update will re-render all relevant components. State can be a medium to communicate between different components as well.


## Preparation Materials

### The Component Lifecycle

The component lifecycle is exactly what it sounds like: it details the life of a component. Like us, components are born, do some things during their time here on earth, and then they die 

But unlike us, the life stages of a component are a little different. Here’s what it looks like:

![](https://cdn-media-1.freecodecamp.org/images/1*U13Mlxz_ktcajaeJCyYkwg.png)


### Mounting

Since class-based components are classes, hence the name, the first method that runs is the constructor method. Typically, the constructor is where you would initialize component state.

Next, the component runs the getDerivedStateFromProps. I’m going to skip this method since it has limited use.

Now we come to the render method which returns your JSX. Now React “mounts” onto the DOM.

Lastly, the componentDidMount method runs. Here is where you would do any asynchronous calls to databases or directly manipulate the DOM if you need. Just like that, our component is born.

### React’s props.children

props.children is a special prop, automatically passed to every component, that can be used to render the content included between the opening and closing tags when invoking a component

### Composition vs Inheritance

React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.

In React using Composition and Props gives you all the flexibility that you would need. React does not say Composition is better than Inheritance. Composition just fits better within the React's component structure.

With the addition of the latest Hooks in React, re-using code is only going to be much easier.




