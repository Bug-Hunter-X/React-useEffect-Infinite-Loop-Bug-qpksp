# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The bug arises from an improperly configured dependency array, leading to infinite re-renders and a potential crash.

## The Problem

The `useEffect` hook in `bug.js` is designed to log the current count to the console. However, the dependency array `[count]` is incomplete.  Because the effect doesn't explicitly list any dependencies, it runs on every render, causing an infinite loop.