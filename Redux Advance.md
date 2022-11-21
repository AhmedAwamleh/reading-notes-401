## Redux is an open-source JavaScript library for managing application state. It is most commonly used with libraries such as React or Angular for building user interfaces.

## Redux Toolkit
was introduced with a purpose to be the standard way to write redux logic. It is said to be an opinionated, batteries-included toolset for efficient Redux development. By using this, you can write all the code you need for your Redux store in a single file, including actions and reducers. Using this you can make your code more readable. Redux toolkit includes all the tools, you want for a Redux application. At the end of the day all you have is less code and faster setups of Redux in every scenario.

## createSlice in Redux Toolkit
createSlice is a higher order function that accepts an initial state, an object full of reducer functions and a slice name. It automatically generates action creators and action types that correspond to the reducers and state.


## This will help to demonstrate on how to implement createSlice, dispatch action and configure store.

### Step 1: Implement createSilce method and export actions and reducer.
### Step 2: Dispatch action by making use of react hooks in functional component.
### Step 3: Configure the store

## What is Redux Toolkit?
Redux Toolkit is our official, opinionated, batteries-included toolset for efficient Redux development. It is intended to be the standard way to write Redux logic, and we strongly recommend that you use it.

## Why You Should Use Redux Toolkit

Redux Toolkit makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, providing good default behaviors, catching mistakes, and allowing you to write simpler code. Redux Toolkit is beneficial to all Redux users regardless of skill level or experience. It can be added at the start of a new project, or used as part of an incremental migration in an existing project.

Note that you are not required to use Redux Toolkit to use Redux. There are many existing applications that use other Redux wrapper libraries, or write all Redux logic "by hand", and if you still prefer to use a different approach, go ahead!

## createSlice

A function that accepts an initial state, an object of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

### Internally, it uses createAction and createReducer, so you may also use Immer to write "mutating" immutable updates:

Parameters
createSlice accepts a single configuration object parameter

initialState
The initial state value for this slice of state.

name
A string name for this slice of state. Generated action type constants will use this as a prefix.

reducers
An object containing Redux "case reducer" functions (functions intended to handle a specific action type, equivalent to a single case statement in a switch).

### The keys in the object will be used to generate string action type constants, and these will show up in the Redux DevTools Extension when they are dispatched. Also, if any other part of the application happens to dispatch an action with the exact same type string, the corresponding reducer will be run. Therefore, you should give the functions descriptive names.

This object will be passed to createReducer, so the reducers may safely "mutate" the state they are given.
