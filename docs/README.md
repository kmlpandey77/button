<h1> SCSS Button</h1>  

SCSS Buttons is a fully customizable CSS button library built using Sass.

## Install

```npm
npm i scss-button --save

```

## File structure
```
your-project/
├── scss
│   └── your-scss.scss
└── node_modules/
    └── scss-button        
        └── scss
```


## Importing
```css
// your-scss.scss

// Option A: Include all

@import "../node_modules/scss-button/scss/button";
```

```css
// your-scss.scss

// Option B: Include parts

// Required
@import "../node_modules/scss-button/scss/variable";
@import "../node_modules/scss-button/scss/options";
@import "../node_modules/scss-button/scss/base";

// Optional
@import "../node_modules/scss-button/scss/shape";
```

## Variable
Every Sass variable in SCSS Button includes the `!default` flag allowing you to override the variable’s default value in your own Sass.

Here’s an example that changes the color for the <body> when importing and compiling:

```css
// your-scss.scss

// Your variable overrides
$primry: red;
$secondary: back;

// SCSS BUTTON
@import "../node_modules/scss-button/scss/button";
```

Here are the variables we include

### Defaults
Some default settings that are used throughout the button library.

Changes to these settings will be picked up by all of the other modules. The colors used here are the default colors for the 
base button (gray). The font size and height are used to set the base size for the buttons. The size values will be used to calculate the larger and smaller button sizes.

```css
$btn-bgcolor: #EEE;
$btn-font-color: #666;
$btn-font-weight: 300;
$btn-font-size: 1.2rem;
$btn-height: 2.2em;
$btn-font-family: Arial, "Noto Sans", sans-serif;
```

### Name
Button Name (ex .button or .btn or whatever you want)
```css
$btn-name: '.button'; //prefix for all classes
```

### Button Colors
`$btn-colors` is used to generate the different button colors. \
Add, edit or remove colors and recompile. \
Each block contains the `name: (background, color)` \
The class is generated using the name: (ex .button-primary)

```css
$btn-colors:(
    primary: ($primary #fff), //.button-prmary
    secondary: ($secondary #fff), //.button-secondary
    /**
    * dark: (#000 #fff), //(ex .button-dark)
    * your-name: (#background #color), //(ex .button-your-name)
    */
);
```

### Button Shapes
`$btn-shapes` is used to generate the different button shapes. \
Add, edit or remove shape and recompile. \
Each block contains the `name: radius` \
The class is generated using the name: (ex .button-rounded)

```css
$btn-shapes: (
  rounded: 0.2em,
  pill: 5em,
);
```

## Uses

### Flat
```html
<button class="button">None</button>
<button class="button button-primary">Primary</button>
<button class="button button-seondary">Seondary</button>

<!-- or -->
<button class="button button-your-name">.button-your-name</button>
```

### Rounded
```html
<button class="button button-rounded">None</button>
<button class="button button-primary button-rounded">Primary</button>
<button class="button button-seondary button-rounded">Seondary</button>
```

### Pill
```html
<button class="button button-pill">None</button>
<button class="button button-primary button-pill">Primary</button>
<button class="button button-seondary button-pill">Seondary</button>
```