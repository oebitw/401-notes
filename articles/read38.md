# Redux - Asynchronous Actions

## Review, Research, and Discussion


1. How granular should your reducers be?

    There should be a separate reducer function for each slice of data. They are combined before being put into the store.



2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

    When your reducer has finished and returned the new application state, asyncDispatch will trigger store. dispatch with whatever action you give to it. You might try using a library like redux-saga.

3. Name a strategy for preventing the above

    Using Redux middleware thunk, allows for evaluating the actions.



------------------------------------------------

## Vocabulary Terms

- **Store**: Holds the whole state tree of the application, only way to change the state inside is to dispatch an action on it.


- **Combined Reducers**: Helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

-----------------------------------------------

## Preparation Materials

**async action**

- Writing an Async Function Middleware# Both of the middleware in that last section were very specific and only do one thing. It would be nice if we had a way to write any async logic ahead of time, separate from the middleware itself, and still have access to dispatch and getState so that we can interact with the store.

**Redux Middleware**

- a Redux store doesn’t know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

**side effects are things like:**

- Logging a value to the console
- Saving a file
- Setting an async timer
- Making an AJAX HTTP request
- Modifying some state that exists outside of a function, or mutating arguments to a function