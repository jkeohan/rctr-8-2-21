# Traffic Light

Objectives:

- Creating and nest Components
- Passing props and how to using them in JSX
- Importing and setting up state
- Updating state and re-rendering the Component

## Working Version

Here is a <a target="_" href="https://n9wzs.csb.app/">working CodeSandBox solution</a> of the app so you can examine the components in React DevTools.

## Starter CodeSandbox

Here is our <a target="_" href="https://codesandbox.io/s/traffic-light-single-app-component-starter-pqrpw">Starter CodeSandbox</a>

### Instructions

- Examine the working live solution and determine the functionality needed
- Examine the HTML in `App.js` as this contains the HTML elements needed for the design 
- All the CSS has been included in `styles.css`
- The `bulbData.js` file contains the data 

### React Architecture 

<img src="https://i.imgur.com/z4SoMzb.png" />
  
<details><summary>bulbData.js</summary>

```javascript
export default [
  {name:'Stop', color: 'red'},
  {name: 'Slow', color: 'yellow'},
  {name: 'Go', color: 'green'},
]
```
</details>


#### Bulb Component

- Create a `Bulb` Component which will be used to render all 3 bulbs
- It will receive the both `color` and `id` as props
- Keep in mind that all 3 Components will need to run some conditional logic that determines if it should render a `black` background or the color that it represents. 
- **HINT**: A Ternary Operator is a good use case to use for the conditional logic. 

#### Button Component

- Create a `Button` Component which will be used to render all 3 buttons 
- It will receive the following props
  - all the data for that specific button 
  - a handleClick function that will update state


#### App Component

- Import `bulbData.js` a as `bulbData`
- Import `useState` into `App` and configure follows: **const [activeBulb, setActiveBulb] = useState({})**
- Import the `Bulb` Component
- Import the `Button` Component
- Create a `handleControls` function that will be passed the object of which button was clicked which it will use to update state.
- Loop over the bulbData and return a `Bulb` Component and pass it the data it needs
- Loop over the bulbData and return a `Bulb` Component and pass it the data it needs
