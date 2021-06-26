# Hooks API

## Review, Research, and Discussion

1) Why do we not need more .html pages in a multi-page React app?

Do not need them thanks to client-side routing libraries, react-router-dom allows to register multiple URLs and their corresponding components in one of the parent nodes of the DOM tree. Then, depending on the URL entered certain nodes are rendered to the DOM and others are not. Single-page-applications still need to get data for different components as components render. They may smaller requests for only the data (typically JSON) that is needed whereas a traditional website would request the entire HTML document again as well as the data. In React, data fetching is done inside of components with functions like componentDidMount or using React hooks.


2) If we wanted a component to show up on every page, where would we put it and why?

Inside the <BrowserRouter />, outside a <Route />

3) What does props.children contain?

Props.children is a special prop, automatically passed to every component that can be used to render the content included between the opening and closing tags when invoking a component. Content passed through props.children can include undefined, null, boolean, a number, a string, a React element or an array of any of these recursively, it can also be a function returning one of these types.


## Vocabulary Terms

- **Composition**: the act of combining parts or elements to form a whole, components are the UI building blocks in React applications like pure functions are the building blocks of function composition.

- **Children/Child Components**: components that are nested within a parent React component (button within a form for example), within the parent components JSX tags.

- **Hash Routing**:Uses the hash in the URL to render the component. Since building a static one-page website, I needed to use this.


- **Link Routing**:Provides declarative, accessible navigation around your application.


## Preparation Materials


### React Hooks


- Hook is a special function that lets you “hook into” React features. For example, allows you to add React state to function components. 

- Hooks let us organize the logic inside a component into reusable isolated units.

- Hooks apply the React philosophy (explicit data flow and composition) inside a component, rather than just between the components.

- Hooks don’t introduce unnecessary nesting into your component tree. They also don’t suffer from the drawbacks of mixins.

- Hooks let you always use functions instead of having to constantly switch between functions, classes, higher-order components, and render props.

- Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context.

- Built-in React Hooks like useState and useEffect serve as the basic building blocks

- The only argument passed to the ```useState()``` Hook is the initial state, if you want to store two different values in state, you call ```useState()``` twice

- ```useState()``` returns a pair of values: the current state and a function that updates it

- Hooks are fully encapsulated — each time you call a Hook, it gets isolated local state within the currently executing component

- They’re not a way to share state — but a way to share stateful logic
- Each Hook may contain some local state and side effects. You can pass data between multiple Hooks just like you normally do between functions. They can take arguments and return values because they are JavaScript functions.
- Unlike render props or higher-order components, Hooks don’t create a “false hierarchy” in your render tree. They’re more like a flat list of “memory cells” attached to a component. No extra layers.


### Hooks Rules :

- When we write React hooks, we should always call them at the top level, and never nest hook calls in any code.

- Also, they should only be called from within React function components.

- This ensures that they’ll always be called in the same order every time. 

*React relies on the order that the hooks are called to return the right data from hooks*.


### What does useEffect do?

*By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed (we'll refer to it as our “effect”), and call it later after performing the DOM updates*


