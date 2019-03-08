# React Hooks - A deeper dive featuring useContext and useReducer
by: ajDevs | 03/07/19
## I know hooks, useState and useEffect. There's more? useReducer and useContext
## Learning Objectives

## Learning Objectives

By the end of this article, you should be able to answer the following questions:

1. What are Hooks? 
1. Other available Hooks
1. What is Context? 
1. How do I implement useContext
1. What is a useReducer?
1. useReducer and a comparison to similar concepts
1. How do I implement useReducer
1. Conceptual tips with useReducer 
( hoping to custom hook-ify useReducer and see if I can throw useContext in or come up with another advanced use case )

## What are hooks?

React has introduced a new API in there most recent release (v16.8.x), the Hooks API. Hooks allow you to use state and other great React features in functional components. No need to write class components. If you're looking for a solid foundation to build upon, start with useState and useEffect. The following link will give you a great introduction to the basics and some insight into why they were created in the first place.
[React Hooks, a primer.](https://testdriven.io/blog/react-hooks-primer/)

## What other hooks are available?

The new Hooks API has 10 [hooks available](https://reactjs.org/docs/hooks-reference.html) for your enjoyment. This article will go over the useContext and useReducer API. When you are comfortable with these hooks, look into the docs for other hooks you can add to your tool belt, or keep a look out for more posts later, on [TestDriven.io/Blog](https://testdriven.io/blog/).



I'll get into useContext first in this part, I just haven't really used context or the useContext API much just yet. I'll bust out useReducer first, but useContext should conceptually come first in the blog. [thumbs up]

## **What is useContext**

## **How is useContext initialized** + examples

## **What is useReducer**

The basic hook useState is extremely useful, as you've seen from my previous post. You can initialize it as many times as you want within an app, as long as you follow rules. Can you initialize useState too many times? Conceptually, nope. But for me, yes. If I initialize useState more than 2 or 3 times in a single component I break out a different, more complex, hook to give my component a *single state object* to use for the component's state management. This hook is a solid useState replacement when more advance state objects are desired in your functional component(s). 

If you are familiar with at least two of the following three concepts, this might just be a walk in the park: 
    - [Redux reducers](https://redux.js.org/basics/reducers)
    - [Array.prototype.reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
    - [useState()](https://reactjs.org/docs/hooks-state.html). 
    
Only familiar with one, or none. Don't worry! I'll break down the similarities with each. Regardless of where you stand, there's valuable information in each comparison.

> If you dont know enough about Redux Reducers, Array.prototype.reduce, or useState, I recommend doing some research by following the links above after reading this article and play around with them! They're wonderful topics with great learning concepts backing each one of them.


Now, imagine if you could initialize the useState hook just once and have access to a state object in your component. Ok, now, imagine if you could just use the Redux reducer switch statement concept in your *functional component(s)*. Ok, still some stares? Not familiar with redux reducers or useState? That's quite alright. Another comparison is with  [Array.prototype.reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce). The useReducer hook looks very similar to the highly beloved higher order function Array.prototype.reduce. (*HOF reduce* from here on out.) 
#### Comparison to Redux Reducer

#### Comparison to useState

#### Comparison to Array.prototype.reduce
The functionality differences between useReducer and Array.prototype.reduce are minute, but the benefit of useReducer has is huge. Much like  Bare with me. The *HOF reduce callback function* is a lot like the first argument to the useReducer hook function. Again, the first argument is a function. Its second argument is *HOF reduce "initialValue" argument* placed after the call back. It is most commonly used with a switch statement inside the reduce block. It even has an accumulator at the end, lets call that accumulator state! 

<!-- We're getting close. The useReducer hooks looks like if useState, Redux reducers, and Array.prototype.reduce all got together and... cut to; they had a baby! They just made a function, if you know what I mean, containing their best qualities or each participant. After, they got together and decided they would willingly give it up thier function baby for adoption. React, desperate after its divorce with class components, was all like, "omg, sooo cute, I want that." So now, its available to React's functional components, not class components, pig. I know that was ridiculous, but makes total sense now right? Get using! -->

The useReducer hook looks a lot like useState. 

```
javascript
const [ state, dispatch ] = useState(reducer, initialState)

```

What is reducer? Lets see what they're looking for.

```
javascript
const reducer = (state, action) => {
    switch (action.type) {
        case 1: return {
            count: state.counter + 1
        }
        case 2: return {
            count: state.counter + 2
        }
        case 3: return {
            count: state.counter + 3
        }
        default: return state
    }
}

```

(testing this out --> ) If you couple useReducer with a custom hook, you can have state for multiple components. Think of useReducer as a reducer in redux. You can get away with just one, but typically you will have multiple reducers with one state object in your redux store. In this case, you'll have multiple state objects, but they will be available all over your app, your react takes control of the store!

## **How is useReducer initialized** + examples

## The custom hook that killed Redux [knife]



