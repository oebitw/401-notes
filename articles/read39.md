# Redux - Additional Topics



1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

     The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.

2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

    by exporting the new data to replace the state from the reducer. The action calling the reducer will be sent as a function rather than an object and then you can dispatch it.

------------------------------------------------

## Vocabulary Terms

**middleware**: middleware provides a third-party extension point between the when an action is dispatched and the moment it reaches the reducer. It needs to be used for asynchronous calls with Redux.

**thunk**: Thunk is a redux middleware that allows you to do async functions in conjunction with Redux.

-----------------------------------------------

## Preparation Materials

**Redux Toolkit**

- What is Redux Toolkit?

    Redux Toolkit is our official, opinionated, batteries-included toolset for efficient Redux development. It is intended to be the standard way to write Redux logic, and we strongly recommend that you use it.

- Redux Toolkit was originally created to help address three common concerns about Redux:

    - "Configuring a Redux store is too complicated"
    - "I have to add a lot of packages to get Redux to do anything useful"
    - "Redux requires too much boilerplate code"

- Toolkit includes:

- A configureStore() function with simplified configuration options. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.


- A createReducer() utility that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the immer library to let you write simpler immutable updates with normal mutative code, like state.todos[3].completed = true.


- A createAction() utility that returns an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.


- A createSlice() function that accepts a set of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.


- The createSelector utility from the Reselect library, re-exported for ease of use.