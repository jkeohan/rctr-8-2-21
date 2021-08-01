
Title: Intro to React<br>
Duration: 1hr+ <br>
Creator:  Joe Keohan<br>

---


# Intro to React.js

<img src="https://i.imgur.com/yt8BVNj.png" width=500/>

## Learning Objectives

* Explain what a frontend framework is and why it is needed for writing more complex applications.
* Explain what React.js is and where it fits in our applications' stack.
* Explain the component model of web development.
* Create and render React components in the browser.

## Framing

### The Rise and Fall of jQuery

I'm sure everyone has either heard or worked with jQuery in their Front End Dev career.  It was first introduced in 2006 and now close to [20 million web sites](https://www.similartech.com/compare/jquery-vs-react-js) have been built using the library vs. the 1 million+ for React.

<img src="https://i.imgur.com/1QmJMVa.png" /><br>

The jQuery `library` was the front end developers tool of choice for quite sometime and many feel it's starting to run it's course. 

More and more developers are opting to use libraries that are also considered  `frameworks`.


### The Birth of the Frontend Frameworks

As the world of front end development and software engineering grows in complexity so does the need to create new tools that:

- facilitate the development process amongst larger teams
- write more reusable code 
- increase the performance of the application

Several years after the birth of jQuery several front end frameworks were introduced that provided a much more structured and opinionated way of writing code.  

Here are a few of the most well known frameworks and when they were introduced.

| Framework | Year Introduced |
| :---: | :---: | 
| Angular | 2009 |
| Backbone | 2010|
| Ember | 2011 |
| React | 2013 |


<!-- <hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 3min

- Think about what a front end framework is and answer the following questions:
  - How is it different than a JavaScript library like jQuery, Lodash, Underscore or Ramda? 
  - Why would we opt to use it?
- Write our you're answer in a slack thread to you'reself
- When asked slack you're answer in the thread created by the instructor

<hr> -->


<!-- <hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 7min

The following questions are based on the article you were asked to read for homework: [javascript-frameworks-vs-libraries](https://skillcrush.com/blog/javascript-frameworks-vs-libraries/) 


Students will be placed in breakout rooms to discuss what a front end framework is and answer the following questions:
  - How is React different than a JavaScript library like jQuery? 
  - What benefit comes from using a framework like React?
  - When would you consider using a library and framework together? 
  
  The group will decide on a single cohesive answer to that question and pick a member to post their answer. 

:thumbsup: Click on the thumbs up when you're done.

When asked slack you're answer in the thread created by the instructor

<hr> -->

### Front End Frameworks

A framework is a library that provides generic functionality and structure and serves as the foundation to build and deploy applications.  

The following are just a few of the most popular front end frameworks mentioned in [https://2020.stateofjs.com](https://2020.stateofjs.com/en-US/technologies/front-end-frameworks/)

- React
- Vue
- Angular
- Ember

Frameworks can help standardize code, give you additional functionality and performance, and can help get you're code off the ground faster.  

### Sites Built On React

First, let's review a few of the most popular web sites built in React:

*   Facebook - They actually built React! 
*   Instagram - It's public feed and internal system are entirely built on React.


As you can imagine they are not the only popular sites built in React.  


<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 2min

Let's take a look at this article  [32 Web Sites Built In React](https://medium.com/@coderacademy/32-sites-built-with-reactjs-172e3a4bed81)

Look over the sites and determine which ones you have used in the past or perhaps use on a daily/weekly basis

When asked slack you're answer in the thread created by the instructor

<hr>

<!-- ### The History of React

As mentioned before Facebook actually created React to meet the demands of the most popular social media platform of it's day. 

*   First used by Facebook in 2011.
*   Adopted by Instagram in 2012.
*   Made open source in May 2013.
*   Not long after React was embraced by the dev community. 

React was born out of Facebook's frustration with the traditional MVC model and:

  * how re-rendering something meant re-rendering **everything** (or just a lot).
  * how it had negative implications on processing power and ultimately user experience, which at times became glitchy and laggy. -->

### What Is React.js

React is a JavaScript `framework` used to craft modern day UI for the front-end in web applications. It essentially takes the UI and breaks it down into reusable `Components`.  

By modeling small reusable `Components` that focus on just rendering a specific portion of the view,  React can improve an app's performance, maintainability, modularity and readability.

<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - React Developer Tools - 5min

Let's take a look at a simple app built in React: [Mars Rebuild](https://02nz9.csb.app/)

Looking at the sites UI we can't really see React.  It's there working under the hook but just not so apparent on the surface.  So let's peel back a layer and see React in action.  

This involves installing [React Chrome Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)

Take a moment to install the tool and then open `DevTools` to confirm the **Components** and **Profile** tabs have been added:

<img src="https://i.imgur.com/KsccFOw.png">

:thumbsup: Click on the thumbs up when you're done.

Now let's take a look at a more advanced app built in React: [Postmates](https://postmates.com/).

<hr>

<!-- ### React Alone Can't Build A App

React can co-exist with other Javascript libraries and frameworks.  If fact there are many helper libraries that developers use quite often like, `Lodash`, `Underscore` or `Ramda` which are great for performing adv JS functionality.  

 -->

### React in MVC

React is only used for the `front end` when buidling an app and would require working with other frameworks to handle 
the `models - (data)` and `controllers - (business logic)` while having React single handedly manage the views.

The MVC architecture is a JavaScript design pattern for building an applications. It isn't the only design pattern being used and others exist such as `MV*`, `MVP`, `MVVM` but the `MVC architecture` is used quite often and represents the following:

- `M stands for Model`
- `V stands for Views` 
- `C stands for Controller.` 

 The `View` is the presentation layer, it’s what the user sees and interacts with in the browser. The `Controller` makes the decisions based on requests and then controls what happens in response, like clicking on links and submitting forms and communicates with the `Model`, which is the database and returns data. 

 `React` is the `View` in this model. 

<img src="https://i.imgur.com/t779Jw9.png" width=600/>

The backed is represented here by `Controller` and `Model` and can be implemented using any backend framework such as:

- Node/Express (unit 3)
- Ruby on Rails / Python & Django (unit 4)
- PHP






<!-- ## The Virtual DOM For Efficiency

The `Document Object Model` or DOM for short is an API that is used to interact with the HTML that is displayed on a page.  The following structure represents the DOM and starts with the `document` object. 

<img src="https://i.imgur.com/qB0cznr.png" width=500/>

If you have ever used `document.getElementById('someid`) or jQuery's `$('#someid`) then you have worked with DOM. 


The Virtual DOM is a representation of the actual DOM and is a staging area for changes that will eventually be implemented. Because of that, React can keep track of changes in the actual DOM by comparing different instances of the Virtual DOM.

  <img src="https://i.imgur.com/xTxgF0b.png" width=500/>

React then isolates the changes between old and new instances of the Virtual
  DOM and then only updates the actual DOM with the necessary changes as opposed to re-rendering an entire
  view altogether which makes React significantly more efficient.


  <img src="https://i.imgur.com/RmHCcDu.png" width=500/> -->


### Getting Started With React

So now it's time to get started with React. For this demo we will be using an online platform called  `CodeSandbox`. 

<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 1min


- Go to [https://codesandbox.io](https://codesandbox.io) and sign  up for a free account
- :thumbsup: Click on the thumbs up when you're done.

<hr>

Here is the starter code we will be working with: [React CodeSandbox Starter](https://codesandbox.io/s/rctr-8-2-21-getting-starter-v05qc?file=/src/index.js)

**Note:** Be sure to fork button on the top right:

<img src="https://i.imgur.com/KQSFfqE.png" width=300/>

<!-- **NOTE:** In order to easily share code, submit homeowrk and work through errors we will be using `CodeSandbox` for this remote course. -->

#### Configuring Our React App
A few things have been removed from this CodeSandbox so that we can focus on:

- Installing the required dependencies (libraries): `(react & reactDOM)`
- Importing the libraries into `index.js`
- Using `ReactDOM.render()` to render our initial content. 

#### Adding Dependencies

Let's add the dependencies first.  On the left side click on `Add dependency` 

<img src="https://i.imgur.com/Q9aLHqN.png" width=300/>

And then search for and add the following:

- `react` - used to create Components
- `react-dom` - used to manage the Virtual DOM
- `react-scripts` - used to transpile the code

Once they have been added it should look like the following.  Take note of the react version as React has gone through several iterations`.  

As of `16.8` React introduced `Hooks` which allowed **Functional Components** to **hook** into functionality previously available in **Class Components**. 

**Hooks** are the way to write modern day React and will use them throughout this class.  

<img src="https://i.imgur.com/60wz4jr.png" width=300/>

#### Setting Up index.js

In the left pane we should see the following.  This is essentially the default folder structure for the React App.

Both the `public` and `src` folders are very important in a React app. The `public` folder is what is sent to the end user and the `src` folder is used to write all our React code. 

<img src="https://i.imgur.com/pHKE3l4.png" width=300/><br>

The one element inside the `public/index.html` file that we need to be aware of right now is:

```html
<div id="root"></div>
```

This will be the element that React mounts to and uses to render the entire app. 

#### Importing The Libraries
Before you can work with React, or any library for that matter, we must import them into the file in which they will be used.  In our case let's import the libraries into `index.js`.

```js
// IMPORT React
import React from "react";
// IMPORT ReactDOM
import ReactDOM from "react-dom";
```

#### ReactDOM.render()
With our libraries in place we can use `ReactDOM.render()` to render either, a `Component` or plain `HTML` to the screen.  

In our basic starter app we will render some basic `HTML` for now.

`ReactDOM.render()` accepts the following two arguments:

- The HTML or Component name to render
- The DOM element we want to mount react to which in our case is:  `<div id="root"></div>`

```js
// GRAB THE ELEMENT WITH AN ID OF ROOT AND STORE IN A VARIABLE CALLED rootElement
const rootElement = document.getElementById("root");
// USE ReactDOM TO RENDER SOME HTML

//                WhHAT TO RENDER    WHERE TO RENDER
ReactDOM.render(<h1>Hello World</h1>, rootElement);
```

We should see our app update to display the following:

<img src="https://i.imgur.com/sY8NkIg.png" width=300/>


We only use `ReactDOM.render()` once when initially `mounting` the React app. 

:question: But what happened the previous HTML? 

<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 3min


Let's take a moment to examine `public/index.html`


- Look for the element with an `id=root`
- Does it have any HTML directly inside of it? 
- Investigate the same element in `Chrome Developer Tools` and we should see the following:

<img src="https://i.imgur.com/kxwtvbn.png" width=300/>

Now, in the HTML, cut the entire element with `<div className=App>` and paste it over the `<h1>` in `index.js`. 

<img src="https://i.imgur.com/y2l6la8.png" width=400/>

React will re-render and our page should display the content.   

Take special note that once the element is rendered that React renamed `className` to `class`.  This happened as the keyword `class` is a reserved word in JS ES6for creating ES6 Classes and so React requires that we define css classes as `className`. 

<img src='https://i.imgur.com/LViMzXN.png' width=500/>

<hr>

### Final Solution

Here is the final [CodeSandbox Solution](https://codesandbox.io/s/seir-831-getting-starter-forked-jogq5?file=/src/index.js:188-372)

### Bonus - ### Becoming A React Developer

Learning React requires that one have an understanding and working knowledge of basic front end technologies, such as: 

- HTML
- CSS
- JavaScript (ES6, ES7, ES8) 

It then opens the door to a whole new world of development tools that are used in the React ecosystem.  

The [React Developer Roadmap](https://hackernoon.com/the-2020-reactjs-developer-roadmap-8q143yan) does a good job of documenting the technologies and concepts that one will be exposed to when working in React.

<img src="https://i.imgur.com/hZOSZbb.png" width=900/>

### Resources

- For an intro to React, watch [this video](https://generalassembly.wistia.com/medias/lr8idjxtx8).
- [Essential JS Design Patterns](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)
