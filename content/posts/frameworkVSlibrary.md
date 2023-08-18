---
title: "Framework VS Library"
date: 2023-08-08T20:24:56+05:30
draft: true
show_reading_time: true
featured_image: "https://images.unsplash.com/photo-1582578598774-a377d4b32223?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2342&q=80"
Tags: ["Tech"]
---

## Developer's life!!!

In our daily development life we will be using different frameworks and libraries. But when asked what's the difference between them, most of them doesn't know. lets take sometime and understand what are these and what's the difference between them.

## What is Library ?

![Library](https://images.pexels.com/photos/1290141/pexels-photo-1290141.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2)

A library in programming can be likened to a mechanic's workshop. You have the spanner, set of tyres, set of decoration items and so on. The mechanic workshop is a collection of tools that vehicles for upgrade or repair purposes.

In our technical terms, A library is a collection of pre-defined/pre-written code that can be reused anywhere in your program. Generally, libraries are focused on narrow scopes such as strings, sockets, and IO, etc. Developers can avoid writing code for functionality that is already written in the library by using it. 

We can create our own libraries. For example:

``` js 
const greet = (name) => {
  return `Hello! welcome to my library ${name}`
}
```
Yeah, this is also a library 😅.

## What is Framework ?

![Framework](https://images.unsplash.com/photo-1565008447742-97f6f38c985c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2831&q=80)

A framework can be likened to Amazon. They have their own way of selling products. If you want to work with them, they dictate the rules on how products are sold. They are like a framework for selling products.

In our technical terms, A framework is like a foundation for developers to build and deploy applications for a particular platform. It contains reusable code written to perform common tasks, with the custom code provided by the developer. Basically it provides the skeleton/structure for your application and you can build on top of it.

## Differences

The primary difference between a library and a framework is the “Inversion of Control.” Simply put, this refers to who is in control of the programming process.

- You are in charge of your applications work when using libraries compared to frameworks. You use libraries when you want to but frameworks most times instruct you on what to use and when to use it.

- Frameworks provide a more comprehensive set of functionality and often include a wide variety of pre-built components. Libraries tend to be more specialized and provide a specific set of functions or tools.

- Frameworks are usually larger in size and may include many more files and classes than libraries, which are usually smaller and more focused.

## Final understanding

Frameworks and libraries are both code written by someone else that helps you perform some common tasks in a less verbose way.

A framework inverts the control of the program. It tells the developer what they need. A library doesn’t. The programmer calls the library where and when they need it.
