---
title: "Jenkins"
date: 2023-01-10T18:18:53+05:30
draft: false
tags: ["Tech"]
featured_image: "/featured_images/jenkins.webp"
---

## What is Jenkins

![Jenkins title](/images/jenkins/Jenkins_title.webp)


Jenkins, the leading opensource tool for Continuous Integration (CI) and Continuous Deployment (CD) processes.

Continuous Integration is a process of building and testing the code whenever the developer pushes the code to source control. Continuous Deployment is the process of deploying the code to multiple environments without any human intervention, thus reducing the time to deliver.



## Advantages of Using Jenkins

  - Open Source
  - Cross-Platform Integration Tool
  - Extensible
  - Thriving Plugin Ecosystem
  - Command Line Interface

## How Jenkins work

- Trigger a build (manual, periodic, poll SCM)
- Get the source code from a repository
- Automatically build and test
- Generate reports (static code analysis, code coverage)
- Notify (Email, Twitter, Jabber, Google Calendar)
- Deploy to servers


## What Is Jenkins Pipeline 

Pipeline in Jenkins is a group of jobs (or events) that are interlinked in a particular sequence. Jenkins Pipeline is a set or suite of plugins that provides support for implementation and integration of Continuous Delivery pipelines into Jenkins.

Every job in the Jenkins pipeline has some dependency on one or more events. Continuous delivery pipeline in Jenkins consists of four states. Build, Deploy, Test, and Release. Each of these states consist of events that execute in a sequence.

## What Is Jenkinsfile

Now that you understand what is Jenkins pipeline, we can dive deeper into the concept. The entire definition of a Jenkins Pipeline is written into a text file called Jenkinsfile. It contains the steps required for running a Jenkins Pipeline. ‘Pipeline as code’ can be implemented using Jenkinsfile and Domain Specific Language (DSL) is used for defining the same.

Jenkinsfile can also be committed to the source control repository of the project. With Jenkinsfile, the CD Pipeline is also treated as a part of the application that is versioned, committed, and reviewed like any other piece of code.

## Important Concepts Of Jenkins Pipeline

  - Pipeline
  - Node
  - Stage
  - Step

## Simple example of jenkins pipeline

```groovy
pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
            }
        }
        stage('Test') { 
            steps {
            }
        }
        stage('Deploy') { 
            steps {
            }
        }
    }
}
```