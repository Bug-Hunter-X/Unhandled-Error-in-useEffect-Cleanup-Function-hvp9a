# Unhandled Error in React Native useEffect Cleanup

This repository demonstrates a bug where an error thrown within the cleanup function of a React Native `useEffect` hook is not handled correctly.  The error is silently swallowed, leading to potential instability in the application.

## Bug Description

The provided code shows a `useEffect` hook that fetches data.  A cleanup function is used to set a `mounted` flag to `false` to prevent memory leaks, and in this example a deliberate error is thrown in the cleanup function. This causes the app to crash silently and a clear error message is not displayed to the developer.

## Solution

The solution involves using a `try...catch` block within the cleanup function to handle potential errors gracefully and provide more informative error messages.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` (or `npx react-native run-ios`).
4. Observe the behavior when the component mounts and unmounts.