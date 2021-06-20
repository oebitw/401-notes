# Props and State

## Review, Research, and Discussion

### 1) Does a deployed React application require a server?

It is not necessary to have a server, React App also works well when integrated into an existing server side app.

### 2) Why do we prefer to test a React application at the behavior rather than the unit level?

When it comes to React components you want to check how your component is rendered and if all props you pass to the component influence the behavior of your component as expected.

### 3) What does npm run build do?

npm run build creates a build directory with a production build of your app.

### 4) Describe the actual composition / architecture of a React application

React application is split into components, it is important that you can add functionality to a component without causing rippling changes through the codebase


## Vocabulary Terms

1) BDD: behavior driven development, a branch of Test Driven Development (TDD), which uses human-readable descriptions of software user requirements as the basis for software tests.

2) Acceptance Tests: conducted to determine if the requirements of a specification or contract are met mounting.

3) Mounting: process by which the operating system makes files and directories on a storage device available for users to access via the computer's file system.

4) build: the process of converting source code into an “executable” bundle by the browser.


## Preparation Materials

### Understanding React `setState`

setState() is the only legitimate way to update state after the initial state setup. Let’s say we have a search component and want to display the search term a user submits.

```
import React, { Component } from 'react'

class Search extends Component {
  constructor(props) {
    super(props)

    state = {
      searchTerm: ''
    }
  }
}
```

We’re passing an empty string as a value and, to update the state of searchTerm, we have to call setState().

```
setState({ searchTerm: event.target.value })

```

### Handling Events

Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.

- With JSX you pass a function as the event handler, rather than a string.


For example, the HTML:

```
<button onclick="activateLasers()">
  Activate Lasers
</button>
```

is slightly different in React:


```
<button onClick={activateLasers}>
  Activate Lasers
</button>
```

Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly. For example, with plain HTML, to prevent the default form behavior of submitting, you can write:

```
<form onsubmit="console.log('You clicked submit.'); return false">
  <button type="submit">Submit</button>
</form>
```
In React, this could instead be:

```
function Form() {
  function handleSubmit(e) {
    e.preventDefault();
    console.log('You clicked submit.');
  }

  return (
    <form onSubmit={handleSubmit}>
      <button type="submit">Submit</button>
    </form>
  );
}
```

### Forms

HTML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state. For example, this form in plain HTML accepts a single name:

```
<form>
  <label>
    Name:
    <input type="text" name="name" />
  </label>
  <input type="submit" value="Submit" />
</form>
```
In react
```
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

### State and Lifecycle

This page introduces the concept of state and lifecycle in a React component. You can find a detailed component API reference here.

Consider the ticking clock example from one of the previous sections. In Rendering Elements, we have only learned one way to update the UI. We call ReactDOM.render() to change the rendered output:

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(
    element,
    document.getElementById('root')
  );
}

setInterval(tick, 1000);
```
**Converting a Function to a Class
You can convert a function component like Clock to a class in five steps:**

1) Create an ES6 class, with the same name, that extends React.Component.

2) Add a single empty method to it called render().

3) Move the body of the function into the render() method.

4) Replace props with this.props in the render() body.

5) Delete the remaining empty function declaration.

```
class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.props.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
```

### Components and Props

Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components. You can find a detailed component API reference here.

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.


### React Testing Library

React Testing Library (RTL) is made of simple and complete React DOM testing utilities that encourage good testing practices, especially one:

The more your tests resemble the way your software is used, the more confidence they can give you. 

In fact, developers tend to test what we call implementation details. Let’s take a simple example to explain it. We want to create a counter that we can both increment and decrement. Here is the implementation (with a class component) with two tests: the first one is written with Enzyme and the other one with React Testing Library.

