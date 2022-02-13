# Scss Architecture

In this project we used this structure for our scss files:

```
|---- scss/
| |---- _main.scss
| |---- utilities/   [abstracts/ was used instead]
| | |---- _functions.scss
| | |---- _variables.scss
| | |---- _mixins.scss
| |---- base/
| | |---- _typography.scss
| | |---- _reset.scss
| |---- components/
| | |---- _header.scss
| |---- pages/
| | |---- _home.scss
```

## 1. Main.scss

The first file our structure is the main.scss file. This file is created in the root of the scss folder and all other files will be imported into this file and then translated into CSS.

## 2. Abstracts folder

This folder holds the functions, variables and mixins files.

### \_functions.scss

The function file allows us to define complex operations that you can reuse throughout your stylesheets. By using the @function at-rule (Written as: `@function <name>(<arguments...>) { ... }`) you can define different functions.

### \_variables.scss

The variables file is used to write custom properties to use later in stylesheets. When writing variables in scss, you must use the `$` at the front of the name. Once you have this, you can refer to this with the name and reuse it anywhere in your css without having to type out the values again and again.

### \_mixins.scss

The mixins file can be used for tedious css by making groups of css declarations you wish to use throughout your site. To create a mixin you use the @mixin direction. For example you can do:

```
@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, .25);
  color: #fff;
}
```

to create a mixin called theme with a variable `$theme` to allow you to pass whatever color you want into the theme.

## 3. Base folder

The base folder is used to hold all things concerning the fonts of your website.

### \_reset.scss

The reset file is used to remove all browser styling from elements.

### \_typography.scss

The typography file is used for the styling of your font to be used throughout your website.

## 4. Components folder

The components folder is used to contain all buttons, headers, footers, etc.

### \_header.scss

The header file is used to format the headers of your website.

## 5. Pages folder

The pages folder is used to look at each individual page's styles.

### \_home.scss

The home file is used to set specific styles and values than the other pages.
