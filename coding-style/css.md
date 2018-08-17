# Your Majesty CSS Guidelines

All CSS on Your Majesty projects are written with SCSS (Sassy CSS). Always use precompilation  tools such as `gulp` or `webpack` to transform `SCSS` to `CSS`.

- **Don't use IDs**  
  Classes are fine, no need to use IDs.
  ```scss
  // no
  #page-container {}

  // yes
  .page-container {}
  ```

- **All CSS should be written in `lowercase` with words separated using dash (`-`).**
  > Note: There are exception to this rule, for instance with React, where everything changes, and class names are usually .camelCaseOkay

  ```scss
  // bad
  .myClassName {}
  .some-class-name--someVariation {}

  // good
  .my-class-name {}
  .my-class-name--some-variation {}
  ```

- **Use _BEM_ notation.**  
  Read: https://en.bem.info/methodology/quick-start/
  ```scss
  .page-hero {}
  .page-hero__title {}
  .page-hero__title--fancy {}
  ```

- **Don't _nest_ blocks.**
  ```scss
  // bad
  .page-hero__title__arrow {}

  // good
  .page-hero__arrow {}
  ```

- **Avoid _greedy selectors_**    
  Always try to write CSS with isolation in mind, you don't want your styles to
  bleed over to areas where they should have no influence. Try to do as little style overwriting as possible.
  ```scss
  // bad
  .blog-post-page {
    // In this instance, we're applying a specific style to
    // all img within a page - too greedy!
    img {
      width: 100%;
      margin-bottom: 32px;
    }
  }

  // better
  .blog-post-page__body {
    // Here, the img style is only affecting the images within
    // the body-section of this page - less generalization!
    img {
      width: 100%;
      margin-bottom: 32px;
    }
  }

  // best
  .blog-post-page__image-container {
    // Here, the img style is completely isolated to a single area
    // of high specificity - no overspill!
    img {
      width: 100%;
      margin-bottom: 32px;
    }
  }
  ```

- **Always use _divisible numbers_**  
  Numbers should always be divisible by 2. When working with design files, you
  will encounter numbers that do not seem correct. Always round up or down to the closest number divisible by 8, or 4 depending on the baseline of the project.

  ```scss
  // bad
  .thing {
    font-size: 13px;
    line-height: 25px;
    margin-bottom: 3px;
    padding: 18px 3px;
  }

  // good
  .thing {
    // Font sizes are OK, as long as the line-height is set correctly
    font-size: 13px;
    line-height: 24px;
    margin-bottom: 4px;
    padding: 16px 4px;
  }
  ```

- **Avoid `!important`**  
  If you find yourself having to add `!important` to your styles, your selectors might be too greedy. Try isolating more.
  > Note: Sometimes !important is unavoidable and useful, such as with .hidden-classes. Just try to stay frosty and use caution okay? Okay.
