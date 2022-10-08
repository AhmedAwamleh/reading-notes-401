## How can we ensure that an effect hook runs only once?
pass an empty array as the second argument to the useEffect hook to tackle this use case.

## Can useState() update more than one state variable at the same time?
useState() is an asynchronous hook and it doesn't change the state immediately, it has to wait for the component to re-render. 
useRef is a synchronous hook that updates the state immediately and persists its value through the component's lifecycle,
but it doesn't trigger a re-render
## Is useState() synchronous?
No.
