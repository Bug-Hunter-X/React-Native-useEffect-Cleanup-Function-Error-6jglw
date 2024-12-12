# React Native useEffect Cleanup Function Error

This repository demonstrates a common error in React Native applications related to the `useEffect` hook's cleanup function.  The issue arises when the cleanup function attempts to access or modify the component's state or props after the component has unmounted. This typically leads to errors, and in some cases, crashes.

## Problem

The `bug.js` file contains a React Native component that uses `useEffect` to set up an interval.  The cleanup function attempts to log the current count even after the component is unmounted, resulting in an error.

## Solution

The `bugSolution.js` file shows the corrected implementation.  It prevents the cleanup function from accessing state after unmount by using a flag to check if the component is still mounted.