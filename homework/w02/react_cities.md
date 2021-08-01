# Intro To State Exercise

So far you've learned the following about React:

- Creating and nesting Components
- Passing props and how to using them in JSX
- Importing and setting up state
- Updating state and re-rendering the Component
- Adding and calling event listeners

Now it's time to put it all together. At a high level you will do the following:

> Using only a single App Component you will implement the logic that allows a user to click on one of 4 small images and then update the DOM to display that image as the large image.

<img src="https://i.imgur.com/M3xQbYR.jpg" width=200/>

## Working Version
Here is a [working version](https://codepen.io/jkeohan/live/850f8454693590e9772f8d0f6c2f44c8) of the app so you have a reference of the base functionality that you are being asked to implement. 

The solution above was implemented using jQuery so there is no React code to inspect via DevTools.  It is meant to provide a working example of the apps functionality. 

## Starter CodeSandbox
Here is our [Starter CodeSandbox](https://codesandbox.io/s/rctr-9-8-20-react-cities-starter-kpsk5)


## Instructions
For this exercise you will do the following:

#### App Component
- Examine the working live solution and determine the functionality needed
- Examine the HTML provided in `src/index.html` as this contains the HTML elements needed for the design
- Determine how best to organize the data needed to render the images
- Create a file called imageData.js that contains the data needed, in this case images
- Using Array.map() loop over the data to create the small images based on the structure you decided
- Render the array of elements 
- Import `useState` into App
- Use one or more instances of `useState` to implement the logic
- Work out the remaining logic needed to implement the design

**Note:** All functionality must be placed within App and no additional Components should be created. 


#### Bonus - Additional State

- Add more state and/or update existing state in order to keep track of which small image was clicked
- Place a green border around the image to indicate that it is the image being displayed.
- Any other previously active image will have it's border color removed
