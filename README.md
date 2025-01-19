# Unhandled JS Exception: undefined is not an object (evaluating '_this.state.variable')
This repository demonstrates a common React Native error: attempting to access a state variable before it's initialized.  The `bug.js` file contains the problematic code, and `bugSolution.js` shows how to fix it. This typically occurs when asynchronous operations (like network requests or timers) modify the state after the component renders initially.

## Problem
The problem lies in accessing `this.state.variable` before the state has a chance to be populated. This often leads to `undefined is not an object` errors. 

## Solution
The solution involves using conditional rendering or lifecycle methods like `componentDidMount` to ensure the state is initialized before accessing it. The `bugSolution.js` file showcases how to correctly handle asynchronous state updates to prevent this error.