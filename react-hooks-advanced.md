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
1. What is a Reducer? (very brief redux overview)
1. How do I implement useReducer
1. Conceptual tips with useReducer 
( hoping to custom hook-ify useReducer and see if I can throw useContext in or come up with another advanced use case )

## What are hooks?

React has introduced a new API in there most recent release (v16.8.x), the Hooks API. Hooks allow you to use state and other great React features in functional components. No need to write class components. If you're looking for a solid foundation to build upon, start with useState and useEffect. The following link will give you a great introduction to the basics and some insight into why they were created in the first place.
[React Hooks, a primer.](https://testdriven.io/blog/react-hooks-primer/)

## What other hooks are available?

The new Hooks API has 10 [hooks available](https://reactjs.org/docs/hooks-reference.html) for your enjoyment. This article will go over useContext and useReducer. When you are comfortable with these hooks, look into the docs and see if there are any other hooks you can add to your tool belt.

The basic hooks, useState and useEffect, are extremely useful. You can initialize them as many times as you want within an app, as long as you follow rules. Can you initialize useState too many times? Conceptually no, but for me, if I initialize useState more than 3-4 times in a single component I break out useReducer to give my component a single state object. (testing this out -->> ) If you couple useReducer with a custom hook, you can have state for multiple components. Think of useReducer as a reducer in redux. You can get away with just one, but typically you will have multiple reducers with one state object in your redux store. In this case, you'll have multiple state objects, but they will be available all over your app, your react takes control of the store!

I'll get into useContext first in this part, I just haven't really used context or the useContext API much just yet. I'll bust out useReducer first, but useContext should conceptually come first in the blog. [thumbs up]

## What is useContext

## **How is useContext initialized** + examples

## What is useReducer

## **How is useReducer initialized** + examples

##



