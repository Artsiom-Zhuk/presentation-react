## What is React?
React is a JavaScript library for building user interfaces.

## What is JSX?
XML-like syntax extension of JavaScript.
JSX can best be thought of as a markup syntax that very closely resembles HTML.
JSX makes writing React components, the building blocks of React UI, easier by making the syntax developers use for generating
these strings of HTML almost identical to the HTML they will inject into the web page. Babel parses JSX syntax, which browsers
cannot understand, and transpiles your source code into JavaScript that is less human friendly but will run in browsers.

## What are the Components?
Components are self-sustaining, independent micro-entities that describe a part of your UI. An application's UI can
be split up into smaller components where each component has its own code, structure, and API.

## Props and State
Components need data to work with. There are two different ways that you can combine components and data: either as props or state.
Props and state determine what a component renders and how it behaves. Let's start with props.

### Props
If components were plain JavaScript functions, then props would be the function input. Going by that analogy, a component accepts 
an input (what we call props), processes it, and then renders some JSX code. Although the data in props is accessible to a component,
React philosophy is that props should be immutable and top-down. What this means is that a parent component can pass on whatever data
it wants to its children as props, but the child component cannot modify its props.

### State
State, on the other hand, is an object that is owned by the component where it is declared. Its scope is limited to the current
component. A component can initialize its state and update it whenever necessary. The state of the parent component usually ends
up being props of the child component. When the state is passed out of the current scope, we refer to it as a prop.

## Class Components and Functional Components
A React component can be of two types: either a class component or a functional component. The difference between the two is evident
from their names.

### Functional Components
Functional components are just JavaScript functions. They take in an optional input which, as I've mentioned earlier, is what we
call props.

### Class Components
Class components offer more features, and with more features comes more baggage. The primary reason to choose class components over
functional components is that they can have state.

## What are React lifecycle methods?
Let’s begin with the lifecycle of a component according to the React docs. There are three particular stages in the lifecycle of
a component, that are important for our lifecycle methods, which I will explain:
-	Mount
-	Update
-	Unmount

### Mount
When React creates an instance of a component and inserts it into the DOM (mounting), the following methods are called:
-	constructor()
-	componentWillMount() / static getDerivedStateFromProps()
-	render()
-	componentDidMount()
ComponentWillMount will be removed with React 17. With React 16.3 there were new lifecycle methods introduced.

### Update
If props or state of a component are changed for whatever reason, an update of the component is performed. However, this means
that the component has to be re-rendered, which causes the following methods to be called:
-	componentWillReceiveProps() /  static getDerivedStateFromProps()
-	shouldComponentUpdate()
-	componentWillUpdate / getSnapshotBeforeUpdate()
-	render()
-	componentDidUpdate()
ComponentWillReceiveProps and componentWillUpdate will be removed with React 17. With React 16.3 there were new lifecycle methods
introduced.

### Unmount
At some point our components will be removed from the DOM again. That process is called unmounting and means that the 
following method is called:
- componentWillUnmount

## The Virtual DOM
In React, for every DOM object, there is a corresponding “virtual DOM object.” A virtual DOM object is a representation of a DOM object, like a lightweight copy.
A virtual DOM object has the same properties as a real DOM object, but it lacks the real thing’s power to directly change what’s on the screen.
Manipulating the DOM is slow. Manipulating the virtual DOM is much faster, because nothing gets drawn onscreen. Think of manipulating the virtual DOM as editing a blueprint, as opposed to moving rooms in an actual house.

So, this is all I wanted to tell you about this topic. Thank you all for your attention!








