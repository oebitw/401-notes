# Context API

## Review, Research, and Discussion

### 1. Describe use cases for useMemo() and useReducer()

useReducer can be used for complex data objects that you need to update different properties within. src (Links to an external site.) useMemo memoizes a value, saving it to the cache and not running it again during re-renders unless the value changes.

### 2. Why do custom hooks need the use prefix?

It’s a convention, and without it react wouldn’t be able to automatically check for violations of rules of hooks. src

### 3. What do custom hooks usually do?

extract component logic into reusable functions src

### 4. Using any list of custom hooks, research and name one that you think will be useful in your applications ?

useWebSocket would be useful when building a game web app that needs to communicate with a websocket api.

### 5. Describe how a hook that fetches API data might work.

We could abstract the logic for fetching the data into a custom hook then call that in useEffect for example on multiple pages if they all need access to data from that api call.


## Vocabulary Terms

- **reducer:** A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change.


## Preparation Materials

### Context API

- **Context** provides a way to pass data through the component tree without having to pass props down manually at every level.

- Before You Use Context :Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

- If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

- Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

- The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.

- Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

- The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.