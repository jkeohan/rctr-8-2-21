# Light Levels Refactor For Redux

## Working Version
Here is a [working version](https://r73sr.csb.app/) of the app so you have a reference of the base functionality that you are being asked to implement. 

It does not contain `Redux`

<img src="https://i.imgur.com/yx9Z8M0.png" width=500/>

## Starter CodeSandbox
Here is our [Starter CodeSandbox](https://codesandbox.io/s/light-levels-redux-starter-7r9l7)

## Instructions
For this exercise you will do the following:

### App Component
- Install redux packages (`react-redux & redux`)
- Add Redux to our App by importing `createStore` from `redux`
- Move the reducer and initial state to as separate file and refactor to work with Redux
- Import the reducer back into App
- Create a `store` and pass it the imported reducer
- Wrap the child components in `Provider`
- Remove any props being passed down to the child components as they will consume state value from the global store directly


#### Controls Component
- Subscribe component to the global store using `connect`
- Create a `mapStateToPropsMap` function that maps state values to their corresponding prop values
- Update the component to use any new mapping names (if needed)
- Dispatch actions

#### Light Component
- Subscribe component to the global store using `connect`
- Create a `mapStateToPropsMap` function that maps state values to their corresponding prop values
- Dispatch actions

