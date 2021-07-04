# Redux - Combined Reducers

# Combined Reducers

![image](https://waftengine.org/public/blog/1B5EE4D5D773F8A-RR.jpg)


1. Why choose Redux instead of the Context API for global state?

    Redux is the industry standard for managing state of large applications, so it is important to know well. It is more optimized for larger projects, because the context API re-renders more often.

2. What is the purpose of a reducer?

    Buffer that sits and protects the application state, changes to state by the components have to be passed through the reducer and have to play by the reducers rules. Reducer is a function that runs every time state needs to be updated, and always returns the new state of the application.

3. What does an action contain?

    Object literals that tell the reducer what is being done to the app, and any data required for the update.

  
4. Why do we need to copy the state in a reducer?

    The reducer needs to be a pure function without any side-effects. It should only take in an action and return the new state.

------------------------------------------------

## Vocabulary Terms

**immutable state**: Immutable state is state that cannot be changed. Immutable objects (for which none of the state can be changed) become important when you are dealing with concurrency, the ability for more than one processor in your computer to operate on that object at the same time.

**time travel in redux**: The Redux DevTools records dispatched actions and the state of the Redux store at every point in time. This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app

**action creator**: is merely a function that returns an action object. Redux includes a utility function called bindActionCreators for binding one or more action creators to the store’s dispatch() function.

**reducer**: is a pure function that takes the current state and an action, and returns the next state. Note that the state is accumulated as each action on the collection is applied to change this state. So given a collection of actions , the reducer is applied on each value of the collection (from left-to-right).

**dispatch**: Dispatch is the act of sending something somewhere. In computer science, this term is used to indicate the same concept in different contexts, like to dispatch a call to a function, dispatch an event to a listener, dispatch an interrupt to a handler or dispatch a process to the CPU.

-----------------------------------------------

## Preparation Materials

**Redux**

**Using combineReducers**:

- The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore .

- The resulting reducer calls every child reducer and gathers their results into a single state object.

- combineReducers will combine all the reducers passed to it into a single reducing function