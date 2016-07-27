# Material Design Shadows

> The paper shadows mixin-library for CSS pre-processors.

![demo](https://cloud.githubusercontent.com/assets/7034281/17182925/1cfc8376-542e-11e6-96ea-a25138b9d32a.png)

## Installation

  * git: `git clone git://github.com/mrmlnc/material-shadows.git`;
  * bower: `bower install --save material-shadows`
  * npm: `npm install --save material-shadows`;

## Supported languages

Support for all popular css preprocessors:

  * [Less](http://lesscss.org/)
  * [Sass](http://sass-lang.com/)
  * [Stylus](http://learnboost.github.io/stylus/)

## Usage

```less
// Less, SCSS, Stylus
@import "lib/material-color";

.my-selector {
  .z-depth(); // equivalent to `.z-depth(2)` and `.z-depth-2dp()`

  // Create class for `transition` property.
  .z-depth-transition();

  // Creating a class to an element in the focused state.
  .z-depth-focus();
}

// Class generator
.shadow {
  .z-depth-classes();
}
```

## Supported options

#### z-depth

**dp**

  * Type: `Number`
  * Default: `2`
  * Available values: 2, 3, 4, 6, 8, 16, 24

Depth shadow.

#### z-depth-classes

**transition**

  * Type: `Boolean`
  * Default: `false`

Create class for `transition` property.

**focus**

  * Type: `Boolean`
  * Default: `false`

Creating a class to an element in the focused state.

## Changelog

See the [Releases section of our GitHub project](https://github.com/mrmlnc/material-shadows/releases) for changelogs for each release version.

## License

This software is released under the terms of the MIT license.
