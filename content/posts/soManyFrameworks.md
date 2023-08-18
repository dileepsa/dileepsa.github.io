---
title: ".NET... So many frameworks"
date: 2023-08-07T19:37:54+05:30
draft: false
show_reading_time: true
featured_image: "https://dotnet.microsoft.com/static/images/illustrations/swimlane-community-documentation.svg?v=n0TqLFDe95LKwHVvtAbNJ4gx-Brix-hfAHbmJvECMgY"
Tags: ["Tech"]
---

## My confusion world 🤷🏻‍♂️.

I have started my work with .NET world with little bit of confusion. When i entered .NET world there are lot of frameworks (.NET, .NET framework, .NET core, .NET standard) feels like padhagattam, padhagattam, padhagattam (ignore if you didn't get it). wait... What is a **framework** ?. Having lot of questions and confusion in mind, i decided to read which i usually avoid. I got a fair sense of what these frameworks are serving to the plate or used to serve historically.

## What is .NET 🤔?
![.NET](https://dotnet.microsoft.com/static/images/illustrations/swimlane-community-documentation.svg?v=n0TqLFDe95LKwHVvtAbNJ4gx-Brix-hfAHbmJvECMgY)

.NET is the free, open-source, cross-platform framework, created by Microsoft, for building many different types of applications. With .NET, you can use multiple languages, editors, and libraries to build for web, mobile, desktop, games, IoT, and more. .NET provides a standard set of base class libraries and APIs that are common to all .NET applications. To extend functionality, Microsoft and others maintain a healthy .NET package ecosystem. NuGet is a package manager built specifically for .NET that contains over 100,000 packages.

## What is .NET framework ?
![.NET Framework](https://dotnet.microsoft.com/static/images/redesign/learn/apps/xamarin.svg?v=N_fhFXVLGtIWZteO-psDLzC_ZY22DmT3-b6XfPh_PDM)

.NET Framework is the original implementation of .NET which was developed by Microsoft in the early 2000s to build Web and Desktop applications for Windows. It allows us to write applications in C#, F# and Visual basic. 

The Framework runs on the Windows operating system. However, some implementations of .NET, such as Mono and DotGNU, are available for other platforms. It is a mature and widely used platform for building various applications.

## What is .NET core

![.NET Core](https://dotnet.microsoft.com/static/images/redesign/learn/what-is-dotnet/cross-platform.svg)

.NET Core is a free, open-source, cross-platform framework for building modern applications, including web, mobile, desktop, gaming, IoT, cloud, and microservices.

One of the key features of .NET Core is its ability to run on multiple operating systems, including Windows, Linux, and macOS. Also, it supports numerous languages, including C#, F#, and VB.NET.

## Difference 🤔?

### .NET Framework
  - The .NET Framework is the first implementation of .NET which works on Windows only.
  - Its source code is public but Microsoft doesn’t accept third party contributions for it.
  - It has a very rich desktop development framework for windows which include Windows Forms and WPF.
  - It can be used with a docker container, its image size is large and can only be deployed on Windows containers.

### .NET Core
  - .NET Core is the latest implementation of .NET which runs on Windows, Linux, and macOS.
  - Its open-source and Microsoft accepts third party contributions to .NET Core.
  - .NET core has integrating the support for windows forms and WPF.
  - It is the best choice to work with docker containers.


## Understood!!!
![Understood](https://dotnet.microsoft.com/static/images/redesign/why-ecosystem.svg)

By reading multiple posts, I got an echo of these different .NET Frameworks. 

In summary, .NET Framework and .NET Core are frameworks for building and running the applications.

.NET Framework is a legacy framework that is serving lot of features from a longer time.

.NET Core is a modern and open source framework that is designed for cross-platform and light weight.

## Chalo one more framework ^^

Finally Microsoft released one more framework which is `.NET5` to remove the confusion with different frameworks. From now on `.NET5` is the unified platform that runs on Windows, Linux, Mac, IOS, Android.