# Routing

## Review, Research, and Discussion

1) Do child components have direct access to props/state from the parent?

Child components have access to state from the parent (this.state) when in a class, and have access to props as a functional component.



2) When a component “wraps” another component, how does the child component’s output get rendered?

It's rendered when there is an update to state.

3) Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?

I don't think so, standalone components have no parents to get props from or children to pass props to.

4) What trick can a parent use to share all props with it’s children

Can pass all the props with the spread operator


## Vocabulary Terms

- **props.children**:used to display whatever you include between the opening and closing tags when invoking a component.
- **composition**: a development pattern based on React’s original component model where we build components from other components using explicit defined props or the implicit children prop.


## Preparation Materials

1) React routing


2) To build routing you need to install react-router, react-router-dom, and react-router-native.
3) Determine which type of router to use, ig. <BrowserRouter> and <HashRouter>.
4) Render router component in the App render function.
5) React Router Component: - <Route path=''/>
<Switch>




### React If

An example of React if:


function SomeComponent({ condition }) {
    return <div>
        {condition ? <span>Yes it is true!</span> : null}
    </div>
}


## ARIA HTML:

ARIA defines semantics that can be applied to elements, with these divided into roles (defining a type of user interface element) and states and properties that are supported by a role. ... Addition of ARIA semantics only exposes extra information to a browser's accessibility API, and does not affect a page's DOM.

## Queries:

Queries are the methods that Testing Library gives you to find elements on the page. There are several types of queries ("get", "find", "query"); the difference between them is whether the query will throw an error if no element is found or if it will return a Promise and retry. Depending on what page content you are selecting, different queries may be more or less appropriate.

## Types of Queries:

- Single Elements
        

    - getBy...: Returns the matching node for a query, and throw a descriptive error if no elements match or if more than one match is found (use getAllBy instead if more than one element is expected).


    - queryBy...: Returns the matching node for a query, and return null if no elements match. This is useful for asserting an element that is not present. Throws an error if more than one match is found (use queryAllBy instead if this is OK).


    - findBy...: Returns a Promise which resolves when an element is found which matches the given query. The promise is rejected if no element is found or if more than one element is found after a default timeout of 1000ms. If you need to find more than one element, use findAllBy.


- Multiple Elements


    - getAllBy...: Returns an array of all matching nodes for a query, and throws an error if no elements match.


    - queryAllBy...: Returns an array of all matching nodes for a query, and return an empty array ([]) if no elements match.


    - findAllBy...: Returns a promise which resolves to an array of elements when any elements are found which match the given query. The promise is rejected if no elements are found after a default timeout of 1000ms.
