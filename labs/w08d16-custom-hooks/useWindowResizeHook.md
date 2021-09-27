# useWindowResize Custom Hook

## Working Version
Here is a [working version](https://8pkrz.csb.app/) of the app so you have a reference of the base functionality that you are being asked to implement. 


<img src="https://i.imgur.com/0BG7mYC.png" width=500/>

## Starter CodeSandbox
Here is the [Starter CodeSandbox](https://codesandbox.io/s/custom-hooks-usewindowsize-starter-681s0?file=/src/App.js). 

The code already contains all the logic to update the window width/heigh values as the screen is adjusted.  The goal of this exercise is to refactor existing  code into an custom hook.  

## Instructions
For this exercise you will do the following:

### useWindowResize Hook
- Create a new file called `useWindowsResize.js`
- Move all the relevant code from `App` into `useWindowsResize.js` 
- Configure is so that it returns the values needed 
- Import the Hook into App and make sure it works

<!-- [Full useWindowResize Solution Code](https://codesandbox.io/s/custom-hooks-usewindowsize-solution-8pkrz?file=/src/useWindowSize.js) -->


### Bonus - Reuse In Another App

Try to refactor this [Starter CodeSandbox](https://codesandbox.io/s/usedataapi-starter-si1ds) to make use of this custom [Custom Data Fetching Hook](https://www.robinwieruch.de/react-hooks-fetch-data) (search page for Custom Data Fetching Hook)


<!-- ### Bonus - Reuse In Another App

- Import the custom `useWindowResize` Hook into the App Component in this [Mars - Inline Style](https://codesandbox.io/s/mars-inline-styles-wpixk?file=/src/Components/App.js) version of the site. 
- Refactor `App` to use the `useWindowsResize` custom hook -->

<!-- ### Bonus - Change Color Based On Changes

Try adding some logic that would change the color of the text based on the following:

- width size increases = green
- width size decreases = red

Here is a [working version](https://ejg9u.csb.app/) of this solution.   -->

<!--  -->
<!-- [Full Change Color Solution Code](https://codesandbox.io/s/custom-hooks-usewindowsize-color-changes-solution-ejg9u?file=/src/useWindowSize.js) -->