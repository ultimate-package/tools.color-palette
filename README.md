The color palette tool
===================

A global function that generates color values for other modules. This component is intended to ease the pain of setting color variables in Sass. It can be used like this:

~~~scss
//scss 
.component {
  color: palette(red, dark);
}

//css output
.component {
  color: #AC0000;
}
~~~

## Installation 

This module can be installed as a Bower package:

    bower install ult-color-palette

## Set up 

Global color variables must first be set in Sass map called `$pallettes`. The `color-palette` function will then use this map to apply the right color values without having to add magic color values like `#333333`. Hopefully this makes remembering color values much easier in large-scale projects.

~~~scss
$palettes: (
    red: (
        base: #992A2D,
        dark: #AC0000
    ),
    grey: (
        base:  #B2B2B2,
        x-light: #F2F2F2,
        light: #E5E5E5,
        mid-light: #CCCCCC,
        mid-dark: #888888,
        dark: #333333,
        x-dark: #111111
    )
);
~~~

Each color in the Sass map requires a `base` color to be set for the `color-palette` function to work properly.


## Acknowledgements

- [Friendlier colour names with Sass maps](http://erskinedesign.com/blog/friendlier-colour-names-sass-maps/)


