# Infinite useEffect Loop in React
This repository demonstrates a common React bug: an infinite useEffect loop caused by a missing dependency in the useEffect hook's dependency array.

## Bug Description
The `useEffect` hook in the `MyComponent` function is designed to log the current value of `count` to the console. However, because the dependency array `[count]` is missing, the effect runs after every render, leading to an infinite loop and potentially crashing the application. 

## Bug Solution
The solution is to include `count` in the dependency array. This ensures that the effect only runs when `count` changes.