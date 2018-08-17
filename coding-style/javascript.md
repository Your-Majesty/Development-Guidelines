# Your Majesty JavaScript Guidelines
YM has worked with several libraries and frameworks throughout the years, and will keep that flexibility open. There is no _one framework to rule them all_ and therefore projects might look different in their setup.  
We do follow a _red thread_ in terms of JavaScript, however, and any project will work with some form of
- **Components**  
  Projects are built up of `components`, which combines together to form the full application. This functionality might be provided through
    - `WebComponents` in the form of `CustomElements`,
    - `React`,
    - custom vanilla implementations, and in rare cases
    - `Angular`

  Although the implementation methods vary, these libraries provide the same base functionality which is: _adding JavaScript sprinkles 🦄✨ to DOM elements_.

- **Services / Globals / Singletons** (most likely)  
  When writing Vanilla JS, we follow a singleton pattern for writing global services that are reachable from within any component, providing useful functionality and exposing global elements.

- **Vendor libraries**  
  Depending on the project, YM will use a set of vendor scripts. The most commonly used are:
  - polyfill.io (https://polyfill.io/v2/docs/)
  - bowser (https://github.com/lancedikson/bowser)
  - TweenMax (gsap) (https://greensock.com/gsap)
  - ThreeJS (https://threejs.org/)
  - PIXI.js (http://www.pixijs.com/)

## Standards

- **Variable and Function Naming**  
  Surprisingly, one of the most difficult tasks for a developer is coming up with good names for various parts of an application. All developers will at some point struggle with this seemingly straight forward part of the job.  
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
        - Use descriptive verbs in functions  
          ```js
          destroyChildhoodDreams()
          setupOffspringForFailure()
          ```

        - Prefix returning functions with 'get'
          ```js
          const numberTotalPotatoes = getTotalPotatoes();
          ```

        - Prefix setting functions with 'set'
          ```js
          setTotalPotatoes(123);
          ```

        - Prefix Booleans with 'can', 'has', or 'is'
          ```js
          const canEatPotatoes = true
          const hasPotatoes = numberTotalPotatoes > 0
          const isPotatoLover = canEatPotatoes && hasPotatoes
          ```
