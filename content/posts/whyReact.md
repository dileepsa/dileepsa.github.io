---
title: "React"
date: 2023-08-30T07:24:26+05:30
show_reading_time: true
draft: true
tags: ["Tech"]
featured_image: "https://www.patterns.dev/img/reactjs/react-logo@3x.svg"
---

## React 

The React.js framework is an open-source JavaScript framework and library developed by Facebook. It’s used for building interactive user interfaces and web applications quickly and efficiently with significantly less code than you would with vanilla JavaScript.

## Why react ?
![why react](https://www.tatvasoft.com/blog/wp-content/uploads/2023/07/Why-Use-ReactJS-_.jpg)

Being a part of the JavaScript language, using React spawns many advantages. Products built with React are simple to scale, a single language used on the server/client/mobile side of things grants outstanding productivity, there are workflow patterns for convenient teamwork, UI code is readable and maintainable, and more. World-leading companies have used React and other JS technologies in some of the top market-defining products (Instagram, Reddit, and Facebook being the most vivid examples).

![usage chart](https://www.peerbits.com/static/fa68b7d565f670b96c43c09b2f844ca3/54b08/most-used-web-frameworks.png)

As per the study made by statista in 2022, Node.js is the most used framework globally, React stands second while Angular ranked 5th on the same list.

## State management in react

![State management](https://assets.toptal.io/images?url=https%3A%2F%2Fbs-uploads.toptal.io%2Fblackfish-uploads%2Fcomponents%2Fblog_post_page%2Fcontent%2Fcover_image_file%2Fcover_image%2F1297529%2Fregular_1708x683_image_0-1967657e3078be54d78ccc4d57eae106-f763757d0bd43e58ff9976083b458547-cb44e66cb24bbf150ab28ea5213e176c.png)

A state is a JavaScript object that represents a part of a component. It changes whenever a user interacts with the application, rendering a new UI to reflect the modifications.

State management refers to the practice of managing React application states. It includes storing data in third-party state management libraries and triggering the re-rendering process each time data is changed.

A state management library facilitates communication and data sharing between React components. Several third-party state management libraries are available today, but Redux and Recoil are two of the most popular.

## Functional components

``` jsx
const Movie = (props) => {
  return (
    <div>
		<p>Martian</p>
    </div>
  )
}
```

**Functional components** are JavaScript functions. Functional components return a single HTML element. To return more elements, you can wrap them in a topmost <div> element.

## Class components

``` jsx
import { Component } from 'react';
class Movie extends React.Component {
  constructor(props) {
    super(props);
    this.state = { currState: true }
  }
  render() {
    <div>
      <p>Lights out</p>
    </div>	
  }
}
```

Class components extend from the React.Component class. React.Component objects have **state**, meaning the object can hold information that can change over the lifetime of the object. They can also respond to lifecycle methods, like ComponentDidMount(), ComponentDidUpdate(), and ComponentWillUnMount().

## React Hooks

![React hooks](https://tsh.io/wp-content/uploads/2020/10/react-hooks-best-practices-lead_.jpg)

In React, hooks are functions that allow you to hook into React state and lifecycle features from function components. This allows you to use React without classes.

There are multiple hooks that react introduced:

- useState
- useEffect
- useContext
- useCallback

## Summary

React is an excellent tool with which to create interactive applications for mobile, web, and other platforms.

React is simple, efficient, clean, and it cuts off a significant time from development. It makes a huge difference when you have a dynamic interface with interactive elements.

React provides a wide variety of features with which we can easily build the UI