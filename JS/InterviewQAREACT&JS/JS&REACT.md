
# JavaScript and React Interview Questions

## Component Basics and JSX
### What is a functional component in React?
Functional components are stateless components written as JavaScript functions. They take props as input and return React elements (JSX).

### What is the difference between a functional component and a class component?
Functional components are simple JavaScript functions, whereas class components are ES6 classes that extend from `React.Component`. Class components have access to lifecycle methods, while functional components use hooks to manage state and lifecycle behavior.

### What is the purpose of keys in React?
Keys help React identify which items have changed, are added, or removed when rendering a list of elements. They provide a unique identity for each element.

### What are refs in React? How are they used?
Refs provide a way to access DOM nodes or React elements directly, typically for imperative operations like managing focus, text selection, or triggering animations.

## React State and Props
### What is the difference between state and props?
State is a local data storage that is mutable and belongs to a component, while props are read-only attributes passed from parent to child components to configure or pass data.

### What are controlled components in React?
Controlled components are form elements (e.g., `<input>`, `<textarea>`, `<select>`) where React controls the state of the input via the component’s state. The value of the form input is derived from the state, and any changes to the input trigger state updates.

### What is the use of `setState` in React?
`setState` is used to update the component's state. It tells React that the state of the component has changed, triggering a re-render with the new state.

### What are higher-order components (HOC)?
HOCs are advanced techniques for reusing component logic. They are functions that take a component and return a new component with enhanced functionality.

## Lifecycle Methods and Hooks
### What are React Hooks? Name a few commonly used hooks.
Hooks let you use state and other React features in functional components. Common hooks include:
- `useState()`: For managing state in functional components.
- `useEffect()`: For handling side effects like data fetching and subscriptions.
- `useContext()`: For consuming React context in functional components.
- `useRef()`: For referencing DOM elements or persisting values across renders.

### Explain the `useEffect()` hook and how it replaces lifecycle methods.
`useEffect()` performs side effects in functional components. It combines the behavior of `componentDidMount()`, `componentDidUpdate()`, and `componentWillUnmount()` in class components. You can control when `useEffect` runs by specifying dependencies.

## Advanced Concepts
### What is the Context API in React, and when would you use it?
The Context API provides a way to pass data (like themes, user information) through the component tree without having to pass props manually at every level. It’s useful for global or shared state across multiple components.

### What is memoization in React? How does `React.memo` work?
Memoization is an optimization technique to improve performance by caching the result of expensive calculations. `React.memo` is a higher-order component that prevents re-renders of functional components if their props haven’t changed.

### What is the difference between `useMemo` and `useCallback`?
`useMemo` is used to memoize the result of a function call, whereas `useCallback` memoizes the function itself. `useMemo` returns a value, and `useCallback` returns a memoized version of the callback function.

### What is the virtual DOM in React?
The virtual DOM is a lightweight representation of the real DOM. When the state changes, React updates the virtual DOM first, compares it with a previous version (diffing), and then updates only the actual DOM elements that changed, improving performance.

## Performance Optimization
### How can you optimize performance in a React application?
Strategies include:
- Using `React.memo` for pure functional components to avoid unnecessary re-renders.
- Using `shouldComponentUpdate()` or `PureComponent` for class components.
- Code splitting with `React.lazy` and `Suspense` to load parts of the application on-demand.
- Avoiding inline functions or objects in render methods.
- Using `useMemo` and `useCallback` to prevent unnecessary computations and function recreation.


