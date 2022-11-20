
## Redux provides
a solid, stable, and mature solution to managing state in your React application. Through a handful of small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a delightfully organized, easy to understand modern JavaScript powerhouse.


## Redux is a predictable state container for JavaScript apps.

It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test. On top of that, it provides a great developer experience, such as live code editing combined with a time traveling debugger.

You can use Redux together with React, or with any other view library. It is tiny (2kB, including dependencies), but has a large ecosystem of addons available.




## Getting Started With Redux
The whole global state of your app is stored in an object tree inside a single store. The only way to change the state tree is to create an action, an object describing what happened, and dispatch it to the store. To specify how state gets updated in response to an action, you write pure reducer functions that calculate a new state based on the old state and the action.


![redux](https://user-images.githubusercontent.com/67606888/202877607-cef1156d-6c2b-4a5a-a455-97823fd6aab9.png)

Instead of mutating the state directly, you specify the mutations you want to happen with plain objects called actions. Then you write a special function called a reducer to decide how every action transforms the entire application's state.

In a typical Redux app, there is just a single store with a single root reducing function. As your app grows, you split the root reducer into smaller reducers independently operating on the different parts of the state tree. This is exactly like how there is just one root component in a React app, but it is composed out of many small components.

This architecture might seem like a lot for a counter app, but the beauty of this pattern is how well it scales to large and complex apps. It also enables very powerful developer tools, because it is possible to trace every mutation to the action that caused it. You can record user sessions and reproduce them just by replaying every action.


## Redux Terms and Concepts

### State Management
![redux2](https://user-images.githubusercontent.com/67606888/202877670-f3d887fb-0bca-4f9a-9113-8ad14cc14bf8.png)


It is a self-contained app with the following parts:

The state, the source of truth that drives our app;
The view, a declarative description of the UI based on the current state
The actions, the events that occur in the app based on user input, and trigger updates in the state
This is a small example of "one-way data flow":

State describes the condition of the app at a specific point in time
The UI is rendered based on that state
When something happens (such as a user clicking a button), the state is updated based on what occurred
The UI re-renders based on the new state

<img width="640" alt="one-way-data-flow-04fe46332c1ccb3497ecb04b94e55b97" src="https://user-images.githubusercontent.com/67606888/202877687-079a7a9e-0ddd-43a7-ba37-2cbd133f918e.png">

However, the simplicity can break down when we have multiple components that need to share and use the same state, especially if those components are located in different parts of the application. Sometimes this can be solved by "lifting state up" to parent components, but that doesn't always help.

One way to solve this is to extract the shared state from the components, and put it into a centralized location outside the component tree. With this, our component tree becomes a big "view", and any component can access the state or trigger actions, no matter where they are in the tree!

By defining and separating the concepts involved in state management and enforcing rules that maintain independence between views and states, we give our code more structure and maintainability.

This is the basic idea behind Redux: a single centralized place to contain the global state in your application, and specific patterns to follow when updating that state to make the code predictable.



## SUMMARY
Redux is a library for managing global application state
Redux is typically used with the React-Redux library for integrating Redux and React together
Redux Toolkit is the recommended way to write Redux logic
Redux uses a "one-way data flow" app structure
State describes the condition of the app at a point in time, and UI renders based on that state
When something happens in the app:
The UI dispatches an action
The store runs the reducers, and the state is updated based on what occurred
The store notifies the UI that the state has changed
The UI re-renders based on the new state
Redux uses several types of code
Actions are plain objects with a type field, and describe "what happened" in the app
Reducers are functions that calculate a new state value based on previous state + an action
A Redux store runs the root reducer whenever an action is dispatched
