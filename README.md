# Sass Hex (to) RGB

> This package is compatible with both SASS and SCSS

A way to convert hex values to rgb in sass. The main reason this package exists is to get raw rgb values (e.g. 255, 255, 255) instead of a rgb value wrapped in a function. We also include functions to convert to rgb and rgba.


# Using
```scss
@use 'sass-hex-rgb' as rgb;
```

> Note: depending on how you resolve your sass imports you might need to import from the `node_modules` folder directly, e.g. `./node_modules/sass-hex-rgb`

# Functions

-   `toValues($colour)`
    ```scss
    $red: #f45333;
    $redRGB: rgb.toValues($red); // "244, 83, 51"
    ```

-   `toRGB($colour)`
    ```scss
    $red: rgb.toRGB(#f45333);
    ```

-   `toRGBA($colour)`
    ```scss
    $redAlpha: rgb.toRGBA(#f45333, $alpha: 0.5); // rgba(244, 83, 51, 0.5);
    ```

> Note: I wanted to add `fromValues` as a function, but was unable to as the overhead of splitting the values and converting to a number is large. If anyone has a better idea please submit a [pr](https://github.com/ghostdevv/sass-hex-rgb/pulls)

# Support
-   Join the [discord](https://discord.gg/2Vd4wAjJnm)<br>
-   Create a issue on the [github](https://github.com/ghostdevv/sass-hex-rgb)
