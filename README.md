# React useEffect: Missing Dependency
This repository demonstrates a common bug in React's `useEffect` hook: forgetting to include variables from the component's scope in the dependency array.  This often results in stale closures, where the effect uses outdated values.

## The Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current `count` to the console. However, the `count` variable is missing from the dependency array.  This means the effect only runs once after the initial render, even though `count` changes on every click.

## The Solution
The `bugSolution.js` file corrects the issue by including `count` in the dependency array. Now, the effect correctly runs whenever `count` updates, showing the current value.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the dependencies.
4. Run `npm start` to start the development server.