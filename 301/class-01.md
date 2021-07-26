# Component Based Architecture

## What is a component?
A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture


## What are the charactistics of a component?
+ Object-oriented view
+ Process-related view
+ Conventional view


## What are the advantages of using component based architecture?
+ **Ease of deployment** − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

+ **Reduced cost** − The use of third-party components allows you to spread the cost of development and maintenance.

+ **Ease of development** − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

+ **Reusable** − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

+ **Modification** of technical complexity − A component modifies the complexity through the use of a component container and its services.

+ **Reliability** − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

+ **System maintenance and evolution** − Easy to change and update the implementation without affecting the rest of the system.

+ **Independent** − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.


# What is Props and How to Use it in React

## What is props short for?

**React is a component-based library** which divides the UI into little reusable pieces. In some cases, those components need to communicate (send data to each other) and the way to pass data between components is by using **props**.
**“Props”** is a special keyword in React, which stands for properties and is being used for **passing data from one component to another**.

## How are props used in React?
+ 1-Firstly, define an attribute and its value(data)
+ 2-Then pass it to child component(s) by using Props
+ 3-Finally, render the Props Data

## What is the flow of props?
React has a different approach to data flow & manipulation than other frameworks, and that’s why it can be difficult at the beginning to understand some concepts like props, state and so on.


# React Tutorial through ‘Passing Data Through Props’

_React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called “components”._

JSX comes with the full power of JavaScript. You can put any JavaScript expressions within braces inside JSX. Each React element is a JavaScript object that you can store in a variable or pass around in your program.

## Inspecting the Starter Code
If you’re going to work on the tutorial in your browser, open this code in a new tab: Starter Code. If you’re going to work on the tutorial locally, instead open src/index.js in your project folder (you have already touched this file during the setup).

By inspecting the code, you’ll notice that we have three React components:

+ Square
+ Board
+ Game

As a next step, we want the Square component to “remember” that it got clicked, and fill it with an “X” mark. To “remember” things, components use **state**.


React components can have state by setting this.state in their constructors. this.state should be considered as private to a React component that it’s defined in. Let’s store the current value of the Square in this.state, and change it when the Square is clicked.


**To collect data from multiple children, or to have two child components communicate with each other, you need to declare the shared state in their parent component instead. The parent component can pass the state back down to the children by using props; this keeps the child components in sync with each other and with the parent component.**


# React Docs - hello world
      ReactDOM.render(
        < h1 >Hello, world!</ h1 >,
        document.getElementById('root')
       );

## Knowledge Level Assumptions
React is a JavaScript library, and so we’ll assume you have a basic understanding of the JavaScript language. **If you don’t feel very confident, we recommend going through a JavaScript tutorial to check your knowledge level** and enable you to follow along this guide without getting lost. It might take you between 30 minutes and an hour, but as a result you won’t have to feel like you’re learning both React and JavaScript at the same time.



# React Docs - introducing JSX
      const element = <h1>Hello, world!</h1>;

This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.


React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React **separates concerns** with loosely coupled units called “components” that contain both. We will come back to components in a **further section**, but if you’re not yet comfortable putting markup in JS, **this talk** might convince you otherwise.

# React Docs - rendering elements
Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

       const element = <h1>Hello, world</h1>;

We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element into a root DOM node, pass both to ReactDOM.render():
   
       const element = <h1>Hello, world</h1>;
      ReactDOM.render(element, document.getElementById('root'));


## Updating the Rendered Element
React elements are **immutable**. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to **ReactDOM.render()**.

# React Docs - Components and props

_Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components. You can find a **detailed component API reference here**._

## Function and Class Components

This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

      function Welcome(props) {
        return < h1 >Hello, {props.name}</ h1 >;
      }


You can also use an **ES6** class to define a component:

       class Welcome extends React.Component {
      render() {
      return < h1 >Hello, { this . props . name}</ h1 >;
    }
    }






