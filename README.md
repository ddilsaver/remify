# remify()

Simple set of Sass mixin and function to quickly convert pixels to rems.
This solution assumes that baseline is 10px, you can override that easily
by changing the `baseline-px` value in the `_remify.scss`.

## Usage

- Quick, one-off pixels to rem value conversion

    font-size: remify(12px);

- Converting entire property

    margin: remify(0 20px 20px 0);

- Converting entire property with a pixel fallback for older browsers
    
    @include rem('margin', 0 20px 20px 0);

# remedy()

Reformatted `remify()` into `remedy()` to accept `rem` values instead of `px` for those silly folks that stopped thinking in pixels. I assume the `baseline-px:` to be `16px` this can be overridden same as above. 

Live demo on codepen: http://codepen.io/ddilsaver/pen/jxFhp

## Usage

- One-off fallback creation for mixed value properties like font:
    
    `font-size:remedy(4rem);` 

    `font: 4rem Helvetica, Arial, sans-serif;`

- If you like manually writing fallbacks 

    `margin: remedy(2rem 1rem 3rem);`

    `margin: 2rem 1rem 3rem;`

- Or let remedy() convert entire properties with a pixel fallback for you
    
    `@include remedy(margin, 2rem 1rem 3rem);`
