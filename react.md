## What is React?

React is a JavaScript library.
It follows the component based approach which helps in building reusable UI components.
It is used for developing complex and interactive web and mobile UI.
Even though it was open-sourced only in 2015, it has one of the largest communities supporting it.

## features of React

1. JSX
2. Components
3. Virtual DOM
4. One-way data-binding
5. High performance

## what is virtual dom?

React uses Virtual DOM exists which is like a lightweight copy of the actual DOM(a virtual representation of the DOM).

## How does virtual DOM actually make things faster?

When anything new is added to the application, a virtual DOM is created and it is represented as a tree. Each element in the application is a node in this tree. So, whenever there is a change in the state of any element, a new Virtual DOM tree is created. This new Virtual DOM tree is then compared with the previous Virtual DOM tree and make a note of the changes. After this, it finds the best possible ways to make these changes to the real DOM. Now only the updated elements will get rendered on the page again.

## How virtual DOM Helps React?

React maintains two Virtual DOM at each time, one contains the updated Virtual DOM and one which is just the pre-update version of this updated Virtual DOM. Now it compares the pre-update version with the updated Virtual DOM and figures out what exactly has changed in the DOM like which components have been changed. This process of comparing the current Virtual DOM tree with the previous one is known as ‘diffing’. Once React finds out what exactly has changed then it updates those objects only, on real DOM.

React uses something called batch updates to update the real DOM. It just means that the changes to the real DOM are sent in batches instead of sending any update for a single change in the state of a component.

This entire process of transforming changes to the real DOM is called Reconciliation.

![Alt text](image.png)

## What is a ReactJS Component?

A Component is one of the core building blocks of React. In other words, we can say that every application you will develop in React will be made up of pieces called components. Components make the task of building UIs much easier. You can see a UI broken down into multiple individual pieces called components and work on them independently and merge them all in a parent component which will be your final UI.
![Alt text](image-1.png)

## functional components

Functional components are simpler and more lightweight.
They are basically JavaScript functions that take props (properties) as arguments and return React elements.
Functional components don't have their own internal state or lifecycle methods.
They are also known as stateless components because they don't manage state.

## class based components

Class components are more feature-rich and were the primary way of creating components in React before the introduction of hooks.
They are ES6 classes that extend from React.Component.
Class components have their own internal state and can have lifecycle methods, such as componentDidMount, componentDidUpdate, etc.
They are also known as stateful components because they can manage state.

![Alt text](image-6.png)

## stateful and stateless

Stateful components (or stateful widgets) are components that manage their own state. Class components are often stateful, as they can hold and update their internal state.
Stateless components (or stateless widgets) are components that do not manage their own state. Functional components are typically stateless, as they don't have internal state.

The use of hooks has led to a trend where functional components are often preferred over class components for their simplicity and ease of understanding.

Hooks, such as useState and useEffect, allow functional components to have local state and perform side effects, making them more powerful and flexible.

Functional components are easier to read, write, and test. They encourage the use of pure functions, making the code more predictable and maintainable.

Class components, however, may still be relevant in certain situations, especially if you are working with an older codebase or have specific use cases that align well with class-based features.

## Use Functional Components with Hooks When

functional components:
Simplicity is a Priority
Reusability of Logic
Consistent Development Style
Performance Considerations

class based components:
Working with Legacy Code
Need for Lifecycle Methods
Inheritance

## What is JSX?

JSX is a shorthand for JavaScript XML. This is a type of file used by React which utilizes the expressiveness of JavaScript along with HTML like template syntax.

## How different is React’s ES6 syntax when compared to ES5?

require vs import
export vs exports
component and function
props
state

## state management in React

State management in React is the process of storing and managing the data that is used to render a React application. It is an important part of any React application, as it allows the application to keep track of its current state and to update the UI when the state changes.

## how to manage state

The best way to manage state in your React application will depend on the specific needs of your application. If you have a small to medium-sized amount of state, the useState hook is a good option. If you have more complex state management needs, the useReducer hook, Context API, or a global state management library may be a better choice.
![Alt text](image-2.png)

There are four main types of state you need to properly manage in your React apps:

Local state
Global state
Server state
URL state
https://www.freecodecamp.org/news/how-to-manage-state-in-your-react-apps/

![Alt text](image-3.png)
![Alt text](image-4.png)
![Alt text](image-5.png)
![Alt text](image-7.png)
![Alt text](image-8.png)

## What are portals in React?

Portal is a recommended way to render children into a DOM node that exists outside the DOM hierarchy of the parent component.

![Alt text](image-9.png)

## synthetic event in React

In React, when you click a button or do something on a webpage, that's called an "event." React helps handle these events in a consistent way across different web browsers.

When you create a React component (like a button), you can add functions to respond to events, like when the button is clicked. React gives you a special kind of event, called a "synthetic event," to make it work smoothly.

## what is context api (avoid prop drilling)

The React Context API is a feature that allows you to share state between components without having to pass props down through the component tree. This can be useful for sharing global state, such as the current user or theme, with components that are deep in the tree.

## use callbackHook in React

The useMemo and useCallback Hooks are similar. The main difference is that useMemo returns a memoized value and useCallback returns a memoized function.

## redux and its three components (action, store and reducer)

Redux is a JavaScript library that helps manage the state of an application. It provides a centralized store for the state that is shared across the entire application. Redux uses events called actions to ensure that the state can only be updated in a predictable fashion.

Actions: Describe what happened, but don't specify how the application's state changes
Store: Stores the application's global state in an object tree
Reducers: it is a pure function that takes the current state and an action as arguments and returns the next state.

## use memo

UseMemo is a hook in React that returns a memoized value. Memoization is a concept in computer science that returns a cached result instead of recomputing a function with a given argument.

## What is Webpack?

Webpack is a famous module builder that we extensively use during our Web Development Journey. It is used for those applications that use Javascript.

Webpack only understands Javascript and JSON. So it converts other frontend files like HTML and CSS into modules with the help of a loader and thus provides a complete frontend solution to us. It internally makes a dependency graph while processing any application.

Diffing is how React decides which DOM elements need to be added or modified. If, between renders, a certain React element stays at the same position in the element tree, the corresponding DOM element and component state will stay the same. If the element changed to a different position, or if it’s a different element type, the DOM element and state will be destroyed.

## what if we remove the dependency array in hook?

If you remove the dependency array in the hook, the effect will only be run once, upon component mount. This is because the hook will not be able to track any changes to the component's state or props, and therefore will not be able to re-run the effect when those changes occur.

## is prop drilling good ? and what are the alternatives?

Prop drilling is a technique in React for passing data from parent components to child components. It can be effective for sharing data, but it can also lead to issues such as: Code duplication, Increased cognitive load, Decreased maintainability, Messy code, Debugging difficulties.
Some alternatives to prop drilling include: React Context, Redux, MobX, Hooks, Composition.


## when is the better to use custom hooks with example
Custom hooks are reusable functions that can be used to simplify component logic and manage local component state. They can also handle specific functionality like form validation or API calls.