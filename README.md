# React useEffect Runs on Every Render

This repository demonstrates a common React bug where the `useEffect` hook runs on every render, even when it shouldn't. This can lead to performance issues and unexpected behavior.

## The Bug

The `useEffect` hook in the `bug.js` file is missing the dependency array.  This means it runs after every render, causing the console log to spam repeatedly.  It should only re-run when the `count` variable changes.

## The Solution

The `bugSolution.js` file provides a corrected version with the dependency array `[count]` added to the `useEffect` hook. This ensures that the effect only runs when the value of `count` changes.