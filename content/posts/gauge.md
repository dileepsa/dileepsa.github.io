---
title: "Gauge"
date: 2022-12-18T20:44:06+05:30
draft: true
description: "ThoughtWorks Product"
featured_image: "/featured_images/gauge.webp"

Tags: ["Tech"]
---

## What is Gauge ?

Gauge is yet another test automation tool that serves many purposes of testing . The founder is ThoughtWorks, the company that also created Selenium and GoCD. Gauge is comparable with Protractor or JUnit extended with Cucumber (if you haven’t heard of these, they are worth checking out).

### Setup 

To start a new project, create a new folder and run ```gauge init python``` in it. This will setup a basic Gauge project.

Gauge supports a total of 5 languges that are c#, java, javascript, python, ruby. Gauge has very good support of vs code. Install the gauge plugin for vs code.

### WRITING THE SPECS

The specs are written in Markdown. Each spec file starts with a title . Next, some steps can be defined that will be run before each scenario. When listing steps, you need to prefix each step with an asterix (*) as in a Markdown list. After that, the actual scenarios can be written. They start with a title . Again, the steps for a scenario should be listed as in a Markdown list. You can also add some tags which can be used to only run certain specs and to search in the HTML reports. Here’s an example specification:


``` md
# Customer Signup

To validate whether the customer signed in or not.

Tags:e2etest

## Customer sign-up

Tags : sign-up, customer

* Sign up a new customer with name "JWorks" email "jworks@ordina.be" and "password"
* Check if the sign up was successful

```

### WRITING THE STEPS

The sentences we wrote in the specs still need to be linked to Python functions . We can do so by simply adding a @step annotation to a python function. It doesn’t matter in which file you put the functions, you’re free to choose how to organize them. As long as they are under the step_impl folder.

### RUNNING THE SPECS

Since the project is setup with python, the tests can be run with 
```bash 
gauge run specs
```

### TAGS

You may have noticed in the spec files that tags can be added. They can be used to run only certain specs.

```bash 
gauge run specs --tags "sign-up"
```

### Hooks

Gauge provides the flexibility to add hooks to the specs, scenarioes and to the whole suite. Gauge has some nice hooks called before and after scenario as well as before and after suite. We can add code that needs to be run before and after cases. We can do setup and cleanup of the test in these cases. 

### REPORTS

The thing that i always liked in the gauge is its reports. To get a HTML report, the plugin has to be installed first: gauge install html-report. That’s about it! After running the specs, a nice HTML report will be outputted to the /reports folder. It shows which tests succeeded and which failed with some additional graphs. In the report you’ll even find how long it took to run a test and each of its steps. There’s also a search functionality to quickly find a certain spec.

![Gauge reports](/images/gauge/gauge-report.jpeg)
