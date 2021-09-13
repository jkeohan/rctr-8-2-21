# React Router

Fork the [Starter CodeSandbox](https://codesandbox.io/s/istocks-starter-9wb38)


Look over the working [Solution](https://vhixt.csb.app/) and examine the app in React Dev Tools to see if you can elicit the structure so that you have a starting point for you app. 

This version of the application can uses both the the hard coded data in [`stock-data.json`](./stock-data.js) or pulling data from an API which you can do by signing up for an API key here [https://financialmodelingprep.com/](https://financialmodelingprep.com/)

Here is your routing table.

| Route | Renders                                   | Component        |
| --------- | ----------------------------------------- | ------------- |
| /      | "This is the Homepage page"                    | Home             |
| /about     | "This is theAabout page"| About |
| /stocks/:symbol     | A single stock                         | Stock      |
| /stocks   | All stocks      | Dashboard    |

Your stock tracking app should have the following features...

## React Architecture

Here is a visual of the react architecture based on the above routing table.

<img src="https://i.imgur.com/E3SWaQS.png" width=600/>

## Header 

No matter what route the user is visiting, they should always see a navigation bar at the top of the window. It should contain links to "Home" and "About" pages.

<img src="https://i.imgur.com/H1bJCVr.png" />

## Home

The Home route is the default route and can be activated by clicking on **iStocks**

<img src="https://i.imgur.com/0CzetM2.png" />

## About (`/about`)

If a user clicks on "About" in the navigation bar, they should be directed to an about page. This is just a static page that displays a description of your app.

<img src="https://i.imgur.com/4QOaX1a.png" />

## Dashboard (`/stocks`)

If a user visits `/stocks` or clicks "Home" in the navigation bar, they should be directed to a dashboard page. This page should list all of the stocks that the user is tracking, specifically their `name` and `symbol`. These stocks should be pulled from [`stock-data.js`](./stock-data.js).

Here a basic rendering of the stocks on the Dashboard component.

<img src="https://i.imgur.com/8AxJshG.png" />

## Stock (`/stocks/:symbol`)

If a user clicks on one of the stocks listed in the Dashboard view, they should be directed to an individual stock show view. This view should display all of a stock's attributes.

<img src="https://i.imgur.com/hwBgDv3.png" />

> The resources listed at the bottom of the [readme](README.md) might come in handy when building this out.



<!-- # Bonus Material: [istocks-bonus](./istocks-bonus.md) -->
