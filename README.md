# Material Design Shadows

> The paper shadows mixin-library for CSS pre-processors.

## Installation

  * git: `git clone git://github.com/mrmlnc/material-shadows.git`;
  * bower: `bower install --save material-shadows`
  * npm: `npm install --save material-shadows`;

## Supported languages

Support for all popular css preprocessors:

  * [Less](http://lesscss.org/)
  * [Sass](http://sass-lang.com/)
  * [Stylus](http://learnboost.github.io/stylus/)

## How to use

Just import the file, which includes mixins in your project.

```less
// Less
@import "lib/material-shadows";
// SCSS
@import "lib/material-shadows"
// Stylus
@import "lib/material-shadows";
```

## Syntax

```less
// Syntax
.example {
  // Full shadow: top & bottom
  .z-depth(@depth);
  // Parameters:
  // - @depth number from a range [1..5] || default: 1

  // Top or bottom shadow
  .z-depth-top(@depth);
  .z-depth-bottom(@depth);

  // Animation
  .z-depth-animation(@depth, @orientation);
  // Parameters:
  //  - @depth number from a range [1..5] || default: 1
  //  - @orientation: 'top' or 'bottom' || default: full

  // Generate helper classes
  .z-depth-class(); // more details in section `Helper classes`
}
```

## Examples

Examples are written using the CSS pre-processor [Less](http://lesscss.org/). If you need examples of using a different language (Sass, Stylus), go to the directory `test/`.

**Simple example**

```less
// Include library
@import "lib/material-color";

// Global header
.site-header {
  ...
  .z-depth(); // or also .z-depth(1);
}

// Article card
.article-card {
  ...
  .z-depth(3);
}

// Navigation bar
.navbar {
  ...
  .z-depth-bottom(); // or also .z-depth-bottom(1);
}
```

**Animation example**

For the convenience in the library added mixin for create animation. The parent selector must contain a class with an mixin of animation. Its syntax is as follows:

```less
// Include library
@import "lib/material-color";

//Article card
.article-list {
  transition: box-shadow .28s cubic-bezier(.4, 0, .2, 1);
  .z-depth-animation(3, top);

  & > .item {
    .z-depth(1); // or also .z-depth();
  }
}
```

HTML markup for `.z-depth-animation()`:

```html
<div class="article-list">
  <article class="item">Article with .z-depth(1)</article>
</div>
```

## Helper classes

You can also create a helper classes for all levels shadows.

```less
// Include library
@import "lib/material-color";

// Generate all levels shadows
.z-depth {
  .z-depth-class(); // Parameters: [@animation, @time, @function]
}

// => (output)
.z-depth-1        { box-shadow: 0 2px 5px rgba(0, 0, 0, 0.16), 0 2px 10px rgba(0, 0, 0, 0.12); }
.z-depth-1-top    { box-shadow: 0 2px 10px rgba(0, 0, 0, 0.12); }
.z-depth-1-bottom { box-shadow: 0 2px 5px rgba(0, 0, 0, 0.16); }
...
.z-depth-5        { ... }
...
.z-depth-animation .z-depth-1,
.z-depth-animation .z-depth-2,
.z-depth-animation .z-depth-3,
.z-depth-animation .z-depth-4,
.z-depth-animation .z-depth-5 {
  transition: box-shadow 0.28s cubic-bezier(0.4, 0, 0.2, 1);
}
```

You can change the animation function. Options for animation:

  * @animation: [true (default) | false];
  * @time: .28s;
  * @function: cubic-bezier(.4, 0, .2, 1);

Default settings are taken from the [Polymer](https://www.polymer-project.org/0.5/docs/elements/paper-shadow.html) project.

## Changelog

See the [Releases section of our GitHub project](https://github.com/mrmlnc/material-shadows/releases) for changelogs for each release version.

## License

This software is released under the terms of the MIT license.
