# Component Based UI

## Review, Research, and Discussion


1) Name 5 Javascript UI Frameworks (other than React)

- Angular
- Vue
- Ember
- SolidJS
- Sencha


2) What’s the difference between a framework and a library?

The key difference between a library and a framework is "Inversion of Control". When you call a method from a library, you are in control. But with a framework, the control is inverted: the framework calls you.

## Vocabulary Terms

1) Rendering

is a process used to turn website code into the interactive pages users see when they visit a website. 

2) Templates

is a predesigned resource that shows the structure for the comprehensive layout and display features of any website. It is provided by various suppliers to help make Web design a lot easier for designers. A website template is also known as a Web page template or page template.

3) State

the outcome of all of the actions that the user has taken since the page is loaded or rendered.” A state is a representation of a system in a given time.

## Preview

1) Which 3 things had you heard about previously and now have better clarity on?

-templating
- node js
- API

2) Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
- react
- redux
- react native

3) What are you most excited about trying to implement or see how it works?

build UI using react


## Preparation Materials

### 1) React Introduction

React is an open-source front-end JavaScript library for building user interfaces or UI components. It is maintained by Facebook and a community of individual developers and companies. React can be used as a base in the development of single-page or mobile applications.

- The smallest React example looks like this:

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

### 2) Introducing JSX

JSX stands for JavaScript XML. JSX allows us to write HTML in React. JSX makes it easier to write and add HTML in React.

```
const element = <h1>Hello, world!</h1>;

```
React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.


In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:

```
const user = 'Josh Perez';
const element = <h1>Hello, {user}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```


you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:

```
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```




### 3) Rendering Elements

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.


Let’s say there is a `<div>` somewhere in your HTML file:

```
<div id="root"></div>
```
We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element into a root DOM node, pass both to ReactDOM.render():

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```


React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().






