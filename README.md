# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  Incorrect usage of the dependency array can lead to an infinite render loop.

## Bug Description
The `useEffect` hook, without a proper dependency array, causes the effect to run after every render.  This creates a cycle where updating state triggers a re-render, which in turn triggers the effect again.  This results in an infinite loop and application crash.

## Bug Solution
The solution involves correctly specifying the dependency array.  Including `count` in the dependency array ensures the effect runs only when the `count` variable changes.