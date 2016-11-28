# SASS Variables


Think of variables as a way to store information that you want to reuse throughout your stylesheet. You can store things like colors, font stacks, or any CSS value you think you'll want to reuse. Sass uses the $ symbol to make something a variable. Here's an example:

New Way:

```scss
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

```

When the Sass is processed, it takes the variables we define for the $font-stack and $primary-color and outputs normal CSS with our variable values placed in the CSS. This can be extremely powerful when working with brand colors and keeping them consistent throughout the site

old way:

```css
body {
    font: 100% Helvetica, sans-serif;
    color: #333;
}
```
# Sass Variable Scope

Sass supports two types of variables: local variables and global variables.

By default, all variables defined outside of any selector are considered global variables. That means they can be accessed from anywhere in our stylesheets. For instance, here’s a global variable:

``` scss
$bg-color: green;
```


On the other hand, local variables are those which are declared inside a selector. Later, we’ll examine how we can customize that behavior. But for now, let’s see our first example.

Here we define a mixin and then the btn-bg-color variable within it. This is a local variable, and is therefore visible only to the code inside that mixin:

``` scss
@mixin button-style {
    $btn-bg-color: lightblue;
    color: $btn-bg-color;
}
```
