# Your Majesty Development Guidelines

Your Majesty strives to provide rulesets that aid in rapid and efficient
development using proven technologies and methods. This guide serves as a
starting point when working on a project within the castle walls.

## Contents
1. Local Development Environment
1. Development Concepts
1. Standards
1. Project Structure and Setup
1. Examples & Templates


## 1. Local Development Environment
- **Editor**  
  Make sure to use an editor suitable for development work, such as:  

    - [Atom](https://atom.io/)
    - [Sublime Text](https://www.sublimetext.com/)
    - [Visual Studio Code](https://code.visualstudio.com/)  

  You can decide what to use for yourself, just make sure the tool works _for you_
  rather than the other way around.


- **NodeJS**  
  Make sure to have [NodeJS](https://nodejs.org/en/) installed on your development machine.
  Node is used by most YM projects to provide precompilation tools and deployment options.  
  More on this later.


- **Docker**  
  Make sure to have [Docker](https://www.docker.com/) installed on your development machine.
  Docker Containers provide portable, secure development environments enabling
  rapid project setup while eliminating "garbage" buildup (various tools and frameworks of varying versions) on your local machine.  
  More on this later.


## 3. Standards
- **Variable and Function Naming**  
  Surprisingly, one of the most difficult pains for a developer is coming up with good names for various parts of an application. All developers will at some point struggle with this seemingly straight forward part of the job.  
  Here are some things to consider when naming your variables and functions:

    - Your `variable` should be _self-documenting_  
      Choose a name that describes its purpose and can be read easily.  
      Long variable names are better than long comments.
      ```js
      // bad
      function gaw () {
        return document.querySelector('.main-applcation-window')
      }
      const w = gaw()
      w.aec()

      // good
      function getMainApplictionWindow () {
        return document.querySelector('.main-applcation-window')
      }
      const mainApplicationWindow = getMainApplictionWindow()
      mainApplicationWindow.animateAndClose()
      ```

    - Your `variable` should _describe its type when possible_  
      Choose a name that, when read, hints at what type of variable it is.  
      ```js
        // Use descriptive verbs in functions
        destroyChildhoodDreams()
        setupOffspringForFailure()

        // Prefix returning functions with 'get'
        const numberTotalPotatoes = getTotalPotatoes();

        // Prefix setting functions with 'set'
        setTotalPotatoes(123);

        // Prefix Booleans with 'can', 'has', or 'is'
        const canEatPotatoes = true
        const hasPotatoes = numberTotalPotatoes > 0
        const isPotatoLover = canEatPotatoes && hasPotatoes
      ```


- **Linting**


- **Testing**  
  As a developer, it is part of your job to make sure your code works.  
  Web developers has a tough job, since we need to take so many different environments into consideration.

  - Test your code in all supported browsers  
    Before pushing your code to the repository, make sure that it runs well in all browsers you support.

  - Automate testing  
    Set up your project to use automated integration testing.

## 4. Project Structure
- NodeJS


- WordPress  
  When setting up a WordPress site, always use [Composer](https://getcomposer.org/) and [Bedrock](https://roots.io/bedrock/) as a starting point.


## 5. Examples & Templates
- Docker/Node/Koa/Contentful/MongoDB
