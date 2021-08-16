[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Korilla React Receipts

Korilla is a Korean barbecue taco truck that makes thousands of hungry customers
happy every year.

Their CEO is thinking of updating their short order tracking system using React.

Build a prototype of this short order receipts tracker.

## Prerequisites

- Creating/Updating State
- Lifting State
- Working with inputs and/or forms
- Working with controlled and uncontrolled inputs

### Starter Code

[CodeSandbox Starter](https://codesandbox.io/s/korilla-receipts-starter-donod?file=/src/App.js)


<!-- Start you server by doing the following:

- open your terminal
- cd into the [./korilla-receipts](./korilla-receipts) folder
- run **npm install** to install all dependencies
- run **npm start** to start the server -->


<!-- You can also choose to work on this codebase using this [CodeSandbox Starter](https://codesandbox.io/s/korilla-receipts-starter-donod?file=/src/App.js) -->


## Requirements

Complete parts 1, 2 and 3.  If you have extra time begin working on the bonus sections in the sequence they are provided. 

Here is a [working example](https://98mru.csb.app/) of the app (Parts 1,2,3 only). 

 ### React Architecture
- Review the full functionality of the app and the working app provided
- Work out the React Architecture and add a link to a google doc [here](https://docs.google.com/spreadsheets/d/1OXuP1i_7NKiDoTKWTBFYj93gWHQO6NqJxeKw1vqPFF0/edit?pli=1#gid=1931350864)

<!-- \(https://docs.google.com/spreadsheets/d/1SVdNiDYhg_6pBJehyekBUKqhZ8cd2Xjc_EMFheVPHio/edit?usp=sharing) -->

**Note:** You can either create a new Google Draw doc or make a copy of the [Cities Of The World](https://docs.google.com/drawings/d/1-VAvWnbCfF8ftR9VzMUIrxeJ4DF2PtJhth179qUO2sI/edit) Google drawing and update it to reflect this specific app.

### React Architecture

#### React Architecture
- Review the full functionality and work out the React Architecture
- Make a copy of the [Cities Of The World](https://docs.google.com/drawings/d/1-VAvWnbCfF8ftR9VzMUIrxeJ4DF2PtJhth179qUO2sI/edit) Google drawing and update it to reflect this specific app.
- Update the [Google Sheet](https://docs.google.com/spreadsheets/d/1OXuP1i_7NKiDoTKWTBFYj93gWHQO6NqJxeKw1vqPFF0/edit#gid=1931350864) with the relevant links

<!-- <img src="https://i.imgur.com/HHc5Jyx.png" /> -->
<!-- <img src="https://i.imgur.com/lI9SAKX.png"/> -->

#### The Component Tree

```
- App
  |
  |__ Form
  |
  |__ Receipts
      |
      |__ Receipt
  
```

## Part 1: Render Receipts

You'll be rendering some receipts. This data should be copied/pasted into a file called receiptData.js and imported into App.js. Then use `useState `create [receipt, setReceipt] and assign receipt to the receiptData array.


```js
const App = () => {
  const [receipt, setReceipt] = useState(receiptsArr)
  //...
}
```

### Receipt Data

Here is a copy of the data needed to render some initial receipts. 

<details>
    <summary><strong>Receipt Data</strong></summary>

```js
const receipts = [
   {
    id:1,
    person: "Karolin",
    order: {
      main: "Burrito",
      protein: "Organic Tofu",
      rice: "Purple Rice",
      sauce: "Green Crack",
      drink: "Korchata",
      cost: 22
    },
    paid: false
  },
   {
    id:2,
    person: "Jerrica",
    order: {
      main: "Rice Bowl",
      protein: "Ginger Soy Chix",
      rice: "Sticky Rice",
      sauce: "Korilla",
      drink: "Korchata",
      cost: 19
    },
    paid: false
  },
   {
    id:3,
    person: "Matt",
    order: {
      main: "Salad Bowl",
      protein: "Organic Tofu",
      rice: "none",
      sauce: "K'lla",
      drink: "Sparkling Blood Orange Soda",
      cost: 20
    },
    paid: false
  }
]
```
</details><br>

### Receipts

The receipts should display the following information:

- person
- order
  - main
  - protein
  - rice
  - sauce
  - drink
  - cost
- paid

![korilla receipts rendered Mark](https://i.imgur.com/pTgXZGO.png)

## Part 2: Searching for receipts

Implement a form that allows you to search the receipts based on person name. Once submitted the app should return only those matching names. 

The inputs used to capture user data should all be `controlled` which requires using `onChange` and the use of `state` to update the inputs. 

## Part 3: Update the receipts

Right now, all the receipts are not paid. Add a click event to the paid field that will toggle the values true or false. 

## Bonus #1: Add a New Receipt Form

Add a new form that will allow the user to add a new receipt that captures all the date needed to display the receipt.  It should also the `paid` property to false by default. 

The inputs used to capture user data should all be `controlled` which requires using `onChange` and the use of `state` to update the inputs. 

## Bonus #2: Add `Paid` and `Not Paid` buttons

Add two buttons that will allow you to easily toggle between receipts that are paid and not paid.  Only display those receipts based on the users selection of those buttons

Here are solutions with this bonus:
- [Justin](https://y9m9l.csb.app/)

## Bonus #3: Add a button that will sort the receipts

Add a button that will sort the receipts by name.  

Here are solutions with this bonus:
- [Justin](https://y9m9l.csb.app/)

## Bonus #4: Add some CSS

Be creative and add some CSS.  Here are previous student examples:

- [Haley](https://i56hg.csb.app/)


## Plagiarism

Take a moment to refamiliarize yourself with the
[Plagiarism policy](https://git.generalassemb.ly/DC-WDI/Administrative/blob/master/plagiarism.md).
Plagiarized work will not be accepted.

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
