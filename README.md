# React Native Uninitialized State Access Bug

This repository demonstrates a common bug in React Native: accessing a state variable before it has been initialized.  This often occurs within `useEffect` hooks or other asynchronous operations.

## Bug Description

Attempting to use a state variable before the `useState` hook has finished setting its initial value will lead to the variable being `undefined`. This can cause errors or unpredictable behavior in your application.  The bug is illustrated in `bug.js`.

## Solution

The solution, shown in `bugSolution.js`, involves checking for the existence of the state variable before using it.  This can be done using optional chaining or a conditional statement.