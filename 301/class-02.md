# React lifecycle

+ 1- Based off the diagram the ‘render’ happens first then the ‘componentDidMount’
+ 2- The first thing happens in the lifecycle of React is the **Mounting**


_When a component is instantiated and inserted into the DOM, it occurs during the compilation phase. The **constructor, the static getDerivedStateFromProps, the view, the componentDidMount, and UNSAFE_componentWillMount** all happen in this order during Mounting._

+ 3- (constructor,render,componentDidMount,React Updates,componentWillUnmount)
+ 4- **componentDidMount** it's a method invoked immediately after a component is mounted.

# React State Vs Props
+ 1-counter application which we will pass the initial count or like a function or display something for the user
+ 2- props pass inside the component  and state is something inside of the componenet 
+ 3- when we change the state inside of our application 
+ 4- an input element inside of the form or check box or select box

# React Docs - State and Lifecycle
## Converting a Function to a Class

How convert a function component to a class in five steps:

+ First thing we should create an **ES6** class, with the same name, that extends **React.Component**.
+  we have to add a single empty method to it called **render()**.
+  Then move the body of the function into the **render()** method.
+  and replace **props** with **this.props** in the **render()** body.
+  the last thing delete the remaining empty function declaration.

## Adding Lifecycle Methods to a Class
In applications with many components, it’s very important to free up resources taken by the components when they are destroyed.

We want to set up a timer whenever the Clock is rendered to the DOM for the first time. This is called “mounting” in React.

We also want to clear that timer whenever the DOM produced by the Clock is removed. This is called “unmounting” in React.

We can declare special methods on the component class to run some code when a component mounts and unmounts:
**These methods are called “lifecycle methods”**

      class Clock extends React.Component {
         constructor(props) {
           super(props);
           this.state = {date: new Date()};
         }

         componentDidMount() {
         }

         componentWillUnmount() {
         }

         render() {
           return (
             < div>
               < h1>Hello, world!</h1>
               < h2>It is {this.state.date.toLocaleTimeString()}.</h2>
             </div>
           );
         }
       }




# React Docs - handling events

Handling events with React elements is very similar to handling events on DOM elements and there are some syntax differences:

+ 1- React events are named using camelCase, rather than lowercase.
+ 2- With JSX you pass a function as the event handler, rather than a string.

 In HTML :

       < button onclick="activateLasers()">
       Activate Lasers
     </button>

In React :

      < button onClick={activateLasers}>
     Activate Lasers
     </button>


Note: we cannot return false to prevent default behavior in React so we must call **preventDefault**

Note: In React we don't need to call addEventListener to add listeners to a DOM element after it is created just provide a listener when the element is initially rendered.

# React Tutorial through ‘Developer Tools’
The React Devtools extension for Chrome and Firefox lets us inspect a React component tree with your browser’s developer tools and let us check the props and the state of your React componentsand after installing React DevTools, you can right-click on any element on the page, click “Inspect” to open the developer tools.

Some extra steps to get it working with CodePen:
+ Log in or register and confirm your email (required to prevent spam).
+ Click the “Fork” button.
+ Click “Change View” and then choose “Debug mode”.
+ In the new tab that opens, the devtools should now have a React tab.



