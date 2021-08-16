<br>
Title: Controlled-Uncontrolled Forms<br>
Duration: 1hr + <br>
Creator:  Joe Keohan<br>

---

# Controlled-Uncontrolled Inputs

<img src="https://i.imgur.com/BIes4H2.png" width=600/>

## Learning Objectives

After this lesson you will be able to:

- Learning in to implement a controlled vs uncontrolled form
- Use the `useRef` Hook to reference an element
- Leverage the `onChange` event to capture and update live input
- Place state in a child Component
- Lift data from child to parent Component

## Framing

Inputs...inputs...are everywhere.  You can't escape them and they are crucial to the success of many sites. 

**Controlled Inputs**
It's probably safe to say that you've created more accounts then you can recall off the top of your head.  Its likely you probably have accounts created for Amazon, Netflix, Instagram, YouTube, Facebook, ect just to name a few. 

Each service requires some level of security. At a minimum a username and password and then for some sites the password must contain some level of complexity include min number of character, upper/lower case, numbers, ect.  

We've all seen some version of the below input that will check off criteria as they are met.  

<img src="https://i.imgur.com/6snHbHU.png" width=600/>

The input above represents a `controlled` input in that it captures each character as it is typed and then run some algorithm to determine if that character meets any one of the stated criteria.  

Of course its more efficient and better UI to use a `controlled` input in this case but that's not true for all inputs. 

An `uncontrolled` input would wait until the user has click submit before it does it's thing. 


## Uncontrolled Inputs

An uncontrolled input has much less overhead as sits back and waits until the user is done typing and clicks the submit button.  

:question: ? - Can you think of a use case for an `uncontrolled` input. 

Here is the starter code we will be working with: [CodeSandbox Starter]() - TBD

For this demo we will be working in `FormUnControlled.js`.

Working with an uncontrolled input requires the use of the `useRef` Hook.  It's a Hook that allows us to `reference` an existing DOM element.  

#### Import `useRef`
Like the `useState` Hook it must be imported from React. 

```js
import React, { useRef } from "react";
```

#### Create a New Instance of `useRef`
Once imported we must create a new instance of `useRef`. Let's also include a console log to see what `useRef` returns. 

``` js
const inputRefEmail = useRef()
console.log('inputRefEmail - ', inputRefEmail)
```


<img src="https://i.imgur.com/teFzbUH.png" width=400/>

As we can see  it returns an object with a single key called `current`. 

#### Assign a `ref` prop
We then assign the element a new property called `ref` and assign it the value of the `inputRef`

```js
<input type="text" ref={inputRef} />
```

Once it's assigned the previous console log will update to show that the current reference is the input.

<img src="https://i.imgur.com/fHHTFA4.png" width=400//>

#### Submitting the Input
Of course we now need the user to click `submit` which requires we add and `onClick` event to the button as well as a supporting `handler` function.   

In this case we will call the function `handleSubmit` since it's being used to submit the input.   For now let's also add a console log to confirm the handler is being executed. 

```js
const handleSubmit = () => {
    console.log('handleSubmit`)
}
```

And now assign the `onClick` to the submit button. 

```js
<input type="submit" value="submit" onClick={handleSubmit} />
```

Time to test out the design.  Try clicking the button and confirm we wee the console log output.  

#### Grabbing The Input

Since we know that useRef has stored a reference to the `input` in the `current` key let's see what that looks like in the console. 

```js
const handleSubmit = () => {
    console.log('handleSubmit', useRefEmail.current)
}
```

<img src="https://i.imgur.com/2ku0wb0.png" />

The way we now return the value stored in the input is to use the `value` key. 

```js
const handleSubmit = () => {
    const value = inputRefEmail.current.value
    console.log('handleSubmit - value', value)
}
```

<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 5min

Now it's your turn to try. 

- Create another instance of useRef called `inputRefPassword`
- Assign it to the password input element
- Console log the captured value in handleSubmit

:thumbsup: - Click on the thumbs up when your done.

<hr>

At this point we need to make use of the captured input as well as clear the input fields. Most likely we would update state in either this Component or a parent Component in order to trigger a re-render to clear the login and take the user to the next page. 

For now let's add some state to the Component and clear the input. 

#### Adding State

Using state requires that it first be imported. 

```js
import React, { useState, useRef } from 'react'
```

And then have the following choices in creating state:

- create multiple instance of state, one for each input
- create a single instance of state to hold both values.  

Let's opt for the second option and create a single instance of state that is assigned an object. 

```js
const Form = (props) => {

  const [login, setLogin] = useState({email: '', password: ''})
  console.log('login -', login)
  //...rest of code
}
```

Refreshing the page will display the state in the console.

<img src="https://i.imgur.com/PLfnZ6h.png" width=500/>

#### Updating State

Now let's update the state value once the button is submitted. 

```js
const handleSubmit = () => {
    setLogin({
        email: inputRefEmail.current.value,
        password: inputRefEmail.current.value
    })
};
```

Once the button is clicked the console should display that state has been updated.

<img src="https://i.imgur.com/wqanfSA.png" width=700/>

#### Clearing the Inputs

## Controlled Inputs

Controlled inputs require a bit more setup than their uncontrolled counterparts.  Essentially state is updated with each keystroke so as to evaluate the captured input against the criteria defined. 

Let's first update App to now import and use the other form. 

```js
// import Form from './FormUnControlled'
import Form from './FormControlled'
```

Some of the configuration needed for this form is identical to the other so let's give you a chance to apply your skills. 

<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 5min

- Import `useState` and set it up as we did before
- Create and setup `handleSubmit` as we did before
- Confirm that the handleSubmit button works by updating state with an `email` and `password` values

:thumbsup: - Click on the thumbs up when your done.

<hr>

#### Adding Control

Controlling the input requires states constant supervision.  In order to ddo this we need to do the following:

- assign a `value` prop to each input and assign the corresponding state value
- add an `onChange` event that will be triggered with each key stroke
- create a new `handler` function for the `onChange` event 

#### Assigning a Value Prop

Let's assign a `value` prop to each input. 

```js
// EMAIL INPUT
<input value = {login.email} />
// PASSWOORD INPUT
<input value = {login.passsword} />
```

What you will notice is that none of your input is captured when typing into the fields. 

The reason is that the inputs are assigning the value based on the state value, which at this point is an empty string. Well that is until we click on `handleSubmit`.  Doing so will automatically update the fields based on what was added to state. 

#### Setting up the Handler and onChange Event

In order to capture every keystroke we need to add an `onChange` event listener to each input and assign the corresponding handler function 

Let's first create the handler.  One thing to consider now is that we are no longer using `useRef` to grab a reference of the input so we need another way to distinguish which input called the function.  We will do so by referencing the `event` objects `target` property.  

This means adding a parameter to handleChange that will pass in the event object. 


```js
const handleChange = (event) => {
    console.log('handleChange - event', event)
}
```

And now we assign the handler to both inputs and pass it the event. 

```js
onChange={() => handleChange(event) }
```

Try typing a sequence character in the email field and we should see the following console output.

<img src="https://i.imgur.com/LrWr71O.png" />

Expanding any one of the event objects will show over 2 dozen keys but the one we are interested in is `target` and it show that the event occurred on this element.

<img src="https://i.imgur.com/7wZoY3J.png" width=300/>

#### Capturing the Input Value

Inside of `handleChange` we can now grab the input value using  `event.target.value`. 

```js
const handleChange = (event) => {
    console.log('handleChange - event', event.target.value)
}
```

Now type in a sequence of characters and we should see just that input. 

<img src="https://i.imgur.com/jNPnZi1.png" width=300/>

Here is the thing though. `handleChange` is being used to capture input for both fields.  We can confirm this by adding another console log that targets: 

```js
console.log('handleChange - event', event.target.computedName)
```

Clicking once in each field will return the following console output.

<img src="https://i.imgur.com/OKoWeXO.png" width=300/>

Let's move onto updating state and see how we can work out the logic to update the appropriate  fields. 

#### Updating State

Since state has been assigned an object we will need to update the key that corresponds to the correct input. We could do so based on the previous `event.target.computedName` value but there is a more efficient way to do this. 


Let's examine the first input element and see if there is anything there that is unique assigned to the element. 

```js
<input
    onChange={() => handleChange(event)}
    value = {login.email}
    type="text"
    className="form-control"
    name="email"
    placeholder="Email Address"
/>
```

I suppose there are 2 things as of now, `name` and `placeholder`.  But name has been assigned the same value as the key in state. 

```js
// INPUT
name="email"
// STATE
const [login, setLogin] = useState({email: '', password: ''})
```

The advantage to using this configuration is that we can take advantage of another ES6 goodie `Object Shorthand`.  We first create a variable that grabs the value of the targets name and then use that as the value for the key name in state. 

```js
const handleChange = (event) => {
    const name = event.target.name
        setLogin({  
        [name]: event.target.value
    })
}
```

If we type several characters in sequence we should see them remain in the input field as well as being updated in state. 

<img src="https://i.imgur.com/df7JiQi.png" width=300/>

So the following two things caught my attention:

- state now only contains a single key of email (*what happend to password?*)
- and the following warning appeared just once

<img src="https://i.imgur.com/Rnan7FT.png" />

:question: - Question: How do we fix the issue with state? 


#### Object Destructuring

The answer is to import all keys that exist in state and then update the key(s) we need to as this time. 
```js
const handleChange = (event) => {
    const name = event.target.name

        setLogin({  
        ...login,
        [name]: event.target.value
    })
}
```

Doing so will capture both inputs and update state

<img src="https://i.imgur.com/hyMMmMI.png" width=400/>

### Update HandleSubmit

HandleSubmit still needs to be updated to call whichever method was passed down in order to lift state and pass the captured values to it's parent in order to so something with the credentials.  

For now we are only going to comment out the `setLogin` code in there as you will be working out this logic in the lab.



### Lab Time

The instructor will provide the lab
