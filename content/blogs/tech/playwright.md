---
title: "Playwright"
date: 2022-10-17T09:56:06+05:30
draft: false
featured_image: "/featured_images/playwright.webp"
Tags: ["Tech"]
---

## What is Playwright framework ?

![Playwright logo](/images/playwright/logo.webp)


Playwright was created specifically to accommodate the needs of end-to-end testing. Playwright supports all modern rendering engines including Chromium, WebKit, and Firefox. Test on Windows, Linux, and macOS, locally or on CI, headless or headed with native mobile emulation. Built by the Microsoft team.

Not only is it versatile and easy to work with, but it has lightning-fast execution speeds and some great features that are unique to the Playwright framework, such as Trace Viewer and Test Generator.

- **Test Generator** : is a browser tool that Playwright provides, which records the actions performed in the browser and generates the equivalent code. This is useful if you want to quickly draft some tests or upskill members of your team who are not so familiar with writing code.

## Why use the Playwright framework?

It’s an open-source framework relatively new to the market but is building up popularity fast. Microsoft maintains it and, as a result, receives regular updates and improvements. If we look at the number of downloads for similar frameworks which have been on the market for a while, you can see Playwright has burst onto the scene.

## Key features of Playwright

**Here are a few of the key features of Playwright**

- Support for cross-browser platforms built on Chromium, WebKit, and Firefox – which includes Chrome, Edge, Firefox, Opera, and Safari.

- Support for cross-platform execution on Windows, Linux, and macOS.

- Support for cross-language, including JavaScript, TypeScript, Python, Java, and .NET – write tests in the environment that suits you while still covering all areas and formats.

- Built with modern architecture and no restrictions – interact with multi-page, multi-tab websites like a real user, and tackle frames and browser events with ease.


## Architecture

So a good way to understand this is to compare it with Selenium – Selenium sends each command as a separate HTTP request and receives JSON responses. So every interaction, such as opening the browser, clicking an element, or sending keys in Selenium, is sent as a separate HTTP request.

As you can imagine, this results in slower execution as we wait for responses and introduces a layer of potential flakiness.

Playwright, on the other hand, communicates all requests through a single WebSocket connection, which stays in place until test execution is completed. This reduces the points of failure and allows commands to be sent quickly on a single connection.

![Playwright vs selenium](/images/playwright/playwright_compare.png)

## Core concepts of Playwright 

Playwright works on three core concepts: browser, context, and page.

- **Browser**: To run the tests, you must initiate the browser. Using Playwright, you can use the object of the Browser   class,  an instance of Chromium, Firefox, or Webkit.

- **Context**: The Playwright framework achieves parallelization using browser contexts. The browser contexts are like  incognito-like profiles isolated within a browser instance.

- **Page**: It is a new tab (or pop window) within a browser context. Every action on the test will be performed on the page.

## It's this easy to create a browser

```c# 
    using var playwright = await Playwright.CreateAsync();
		await using var browser = await playwright.Webkit.LaunchAsync();
		await using var context1 = await browser.NewContextAsync(playwright.Devices["iPhone 6"]);
		var page = await context1.NewPageAsync();
		IResponse? response1 = await page.GotoAsync("https://www.google.com");
```

We used playwright in C#.net And it is simple to work with playwright and pretty straight forward.

- Playwright has an extension for VS code 