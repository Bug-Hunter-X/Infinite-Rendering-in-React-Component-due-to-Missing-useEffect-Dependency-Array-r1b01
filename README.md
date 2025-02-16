# Infinite Rendering Bug in React

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.  The `MyComponent` initially renders correctly, but subsequently enters an infinite render loop due to the missing dependency array in the `useEffect` hook. This is because the effect runs after every render, triggering a state update that leads to another render. The solution involves adding `[count]` as the dependency array to the `useEffect` hook, ensuring the effect only runs when the `count` state variable changes.

## How to reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs and the browser behavior to verify the infinite rendering.  The console logs will show the component rendering continuously. 