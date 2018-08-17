# Your Majesty Development Guidelines

Your Majesty strives to provide loose rulesets that aid in rapid and efficient
development using proven technologies and methods. This guide serves as a
starting point when working on a project within the castle walls.

## Contents
1. Local Development Environment
1. Development Concepts
1. Coding Style
1. Testing
1. (Later bae) Project Structure and Setup
1. (Later bae) Examples & Templates

## 1. Local Development Environment
- **Editor**  
  Make sure to use an editor suitable for development work, such as:
    - [Atom](https://atom.io/)
    - [Sublime Text](https://www.sublimetext.com/)
    - [Visual Studio Code](https://code.visualstudio.com/)  

  Make sure the tool works _for you_ rather than the other way around.  
  Your editor should have linting capabilities.

- **NodeJS**  
  Make sure to have [NodeJS](https://nodejs.org/en/) installed on your development machine.
  Node is used by most YM projects to provide precompilation tools and deployment options.  

- **Docker**  
  Make sure to have [Docker](https://www.docker.com/) installed on your development machine.
  Docker Containers provide portable, sandboxed development environments enabling
  rapid project setup while eliminating "garbage" buildup (various tools and frameworks of varying versions) on your local machine.  

## 2. Development Concepts
At YM, we strive to make code that is reusable, portable, and self-documenting.

Before starting work on a project at YM, ensure that you have basic understanding of the following concepts:
- **Class-based Programming (or OOP)**  
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes

- **Singletons**  
  A singleton is an instance of a `class` or other feature rich service that exists as a single entity and is not supposed to be initiated more than once.  
  A common pattern for this in JS looks like this:
  ```js
  const MyCoolSingleton = (() => {
    const data = []

    function doStuff (abc) {
      data.push(abc)
    }

    const controller = {
      doStuff
    }
    return controller
  })()
  ```
  In this example, the instance of the singleton is wrapped in a self-executing anonymous function, creating a contained scope and single instance.

- **W.E.T vs D.R.Y code**  
  https://en.wikipedia.org/wiki/Don%27t_repeat_yourself

The next segment contains in-depth examples on how specific code is to be written.

## 3. Coding Style
- **JavaScript**  
  Please see the [JavaScript Development Guidelines](coding-style/javascript.md)

- **CSS**  
  Please see the [CSS Development Guidelines](coding-style/css.md)


## 4. Testing
  As a developer, it is your responsibility to make sure your code works across multiple devices and screen sizes.

  - **Test your code in all supported browsers**  
    Before pushing your code to the repository, make sure that it runs well in all browsers you support. Create graceful fallbacks for browsers with less features.

  - **Automate testing**  
    You could set up your project to use automated integration testing which runs before or after code push.

## 5. (Later bae) Project Structure
WIP
- NodeJS

- WordPress  
  When setting up a WordPress site, always use [Composer](https://getcomposer.org/) and [Bedrock](https://roots.io/bedrock/) as a starting point.


## 6. (Later bae) Examples & Templates
WIP
