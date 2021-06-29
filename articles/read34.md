# `<Login/>` and `<Auth/>`

## Review, Research, and Discussion


### 1. Why is the Context API useful?
  
Context API is useful because it can help to make information globally available in the app rather than having to pass it in props to each individual child element.

### 2. Can a component outside of a provider get its context?
  
Yes, any component inside the app can get the context as long as it is passed properly and imported at the top of the target page.

### 3. What are some common use cases for  using the Context API?

Needing to pass functions that need to be available in multiple places.

### 4. Describe “Context Hell”

When using the context API, splitting global state properties so as not to share a “god object” creates “Context hell,” a layer of countless contexts wrapping your React application


## Vocabulary Terms

**global state**: provides a way to pass data through the component tree having to pass props down manually at every level, managing state in multiple components that are not directly connected

**global context**: is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component: class App extends React.

**provider**: React uses provider pattern in Context API to share data across tree descendants

**consumer**:  consumer takes a child as a function and that function returns a node.


## Preparation Materials

### what is role based access control?
  - It restricts network access based on a person's role within an organization
  - You can designate management or employee roles that allow certain privileges.
  - Having roles reduces administrative work, as a new employee can be assigned automatically by job title/function, and can decrease unnecessary access to sensitive information/documents.

### React-cookie library 

- it's a Javascript object with all your cookies. The key is the cookie name.

- React way of using and saving cookies

