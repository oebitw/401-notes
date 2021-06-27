# Custom Hooks


## Review, Research, and Discussion

1. What does a component’s lifecycle refer to?

Life cycle is a predefined react function that will be called at specific time of the component life cycle.

2. Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

Because it will prevent recreation of a function.

3. Why are functional components preferred over class components?

Less code, easy to read and test.

4. What is wrong with the following code?

Using useEffect inside a loop.+



## Vocabulary Terms

- **state hook**: is a Hook that lets you add React state to function components.
- **effect hook**: lets you perform life cycle methods in function components.
- **reducer hook**: used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.



## Custom Hooks React

A custom hook allows you to extract some components logic into a reusable function. A custom hook is a Javascript function that starts with use and that call can other hooks. ... We are just refactoring our code into another function to make it reusable.

### Using a Custom Hook
In the beginning, our stated goal was to remove the duplicated logic from the FriendStatus and FriendListItem components. Both of them want to know whether a friend is online.

### useToggle
Basically, what this hook does is that, it takes a parameter with value true or false and toggles that value to opposite. It's useful when we want to take some action into it's opposite action.

### useAuth
A very common scenario is you have a bunch of components that need to render different depending on whether the current user is logged in and sometimes call authentication methods like signin, signout, sendPasswordResetEmail, etc.

## Rules of Hooks
1. Only Call Hooks at the Top Level.
2. Only Call Hooks from React Functions.
3. Don’t call Hooks from regular JavaScript functions.