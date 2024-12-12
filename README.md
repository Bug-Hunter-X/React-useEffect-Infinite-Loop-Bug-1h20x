# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an improperly configured dependency array, leading to an infinite loop and a stack overflow error. The solution shows how to correctly use the dependency array to avoid this issue.

## Bug Description
The provided code uses the `useEffect` hook without a properly defined dependency array.  This causes the effect to run on every render, creating an infinite loop because updating `count` causes a re-render, which then triggers the effect again, and so on.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console and browser for the infinite loop and error messages.

## Solution
The solution correctly specifies the dependency array to prevent the infinite loop.  The effect only runs when the `count` value changes, resolving the problem.