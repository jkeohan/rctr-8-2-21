# Traffic Light

So far you've learned the following about React:

- Creating and nesting Components
- Passing props and how to using them in JSX
- Importing and setting up state
- Updating state and re-rendering the Component
- Adding and calling event listeners

Now it's time to put it all together. At a high level you will do the following:

> Create a TrafficLight Component that will implement the functionality based on the working solution. 

## Working Version
Here is a [working version](https://1sj6y.csb.app/) of the app so you have a reference of the base functionality that you are being asked to implement. 

## Starter CodeSandbox
Here is our [Starter CodeSandbox](https://codesandbox.io/s/rctr-9-8-20-traffic-light-single-app-component-starter-pqrpw?file=/src/App.js)

## Instructions
For this exercise you will do the following:

#### TrafficLight Component
- Examine the working live solution and determine the functionality needed
- Examine the HTML provided in `src/index.html` as this contains the HTML elements needed for the design
- Determine how best to organize the data needed to create the control panel and traffic bulbs
- Create a file called bulbData.js that contains the above data however you decided to organize it
- Create a `TrafficLight` Component 
- Import `useState` into `TrafficLight`
- Work out the remaining logic needed to implement the design

#### App Component
- Import the data into App.js
- Import the `TrafficLight` Component 
- Render a single `TrafficLight` Component and pass it the data it needs 

**Note:** App will render only a single instance of the TrafficLight Component.  Therefore, in App, do not loop over the array of data and create multiple instances. 

### Bonus - Bulb Component

- Create a new `Bulb` Component that will render the a single bulb
- Pass the `Bulb` Component the color it needs based the state of the application
