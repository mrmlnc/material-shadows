Material Design Shadows
==============

The paper shadows, based on [Google's Material Design](http://www.google.com/design/spec/layout/layout-principles.html), for use in your project.



Support
--------------

Support for all popular css preprocessors: [Less](http://lesscss.org/), [Sass](http://sass-lang.com/) and [Stylus](http://learnboost.github.io/stylus/).



How to use
--------------

Just import the file, whitch includes variables colors in your project.

**Less:**

````Less
  @import "lib/material-shadows";
````

**Sass:**

````Sass
  @import "lib/material-shadows";
````

**Stylus:**

````Stylus
  @import "lib/material-shadows";
````

**The build variable:**

`(.|@include|none)(prefix)-z-depth-(depth)-(orientation)`

  - **(.|@include|none)** - Sign of the variable in the preprocessor.
  - **(prefix)** - The prefix variable. Namespace of your variables and variables of the library. (With `material-shadows-prefixed` and without `material-shadows`)
  - **(depth)** - Depth 1..5.
  - **(orientation)** - None, Top or Bottom.

**Example (Less):**

````Less
  @import "lib/material-color";

  .example-1 {
    .z-depth();
    .z-depth-animation(3);
  }

  .example-2 {
    .z-depth-top(1);
    .z-depth-animation(5, top);
  }
````

**Settings**

````Text
  // If True, then will be CSS classes, type: .z-depth-*
  z-depth-css =                         [true | false (default)];
  z-depth-browser-prefix =              [true | false (default)];
  z-depth-animation =                   [true (default) | false];
  z-depth-animation-time =              .28s;
  z-depth-animation-function =          cubic-bezier(.4, 0, .2, 1);
````
