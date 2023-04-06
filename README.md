# Flexspan Grid System

A different kind of Grid System that does not care about IE (Internet Explorer) and has adjustable breakpoints that match your project.

[Documentation](https://brockenstein.github.io/Flexspan-Grid-System/)

Note: This is not just a pre-compiled CSS library that you add to your project but SASS/SCSS partials that you import to your project and customize by modifying SASS variables and compile as part of your project. So this will require a preprocessor. For those who are not command line inclined I personally love [Scout-App](https://scout-app.io/) which is a visual preprocessor or if you like VS Code you could use [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=glenn2223.live-sass).

## Usage
<b>How to set up Flexspan for your project</b>

1. Download the latest release and place the scss partials on the same server as your project's main scss so that it can compile.

2. Add the following code to your main scss in your project. (Note: you may need to adjust the file path if you put the scss partials in a different directory than your main scss.)

    ```
    
        // Breakpoint mixin used with the Flexspan Grid System
        @mixin breakpoint($break) {
            @media screen and (min-width: $break) {
                @content;
            }
        }

        // Breakpoints you may use across the site within mixins
        $xxs: 360px;
        $xs: 480px;
        $s: 550px; 
        $sm: 600px;
        $m: 768px;
        $ml: 960px;
        $l: 1024px;
        $xl: 1200px;
        $xxl: 1400px; 
        
        // Breakpoints you plan on using with the Flexspan Grid System
        $breakpointsUsedForGrid:
        "s" $s,
        "m" $m,
        "l" $l;
        
        // CSS Variable
        // NOTE: You can not add SCSS variables to CSS variables, however you can use CSS variables in SCSS mixins
        :root {
            --fs-spacing-col: 15px;
            --fs-spacing-row: 15px;
        }
        
        // Importing the mixings for the Flexspan Grid System
        @import "_flexspan-grid-mixins", "_flexspan-grid-classes";
    ```

    3. Use the [Documentation](https://brockenstein.github.io/Flexspan-Grid-System/) to use the differnt classes in your HTML





# Table of Contents
* [Intro](https://brockenstein.github.io/Flexspan-Grid-System/#intro)
* [How To Use](https://brockenstein.github.io/Flexspan-Grid-System/#instuctions)
* [12 Grid System](https://brockenstein.github.io/Flexspan-Grid-System/#grid-system)
* [Breakpoints](https://brockenstein.github.io/Flexspan-Grid-System/#breakpoint)
* [Nested Grids](https://brockenstein.github.io/Flexspan-Grid-System/#nested-gril)
* [Fluid](https://brockenstein.github.io/Flexspan-Grid-System/#fluid)
* [Forced Row](https://brockenstein.github.io/Flexspan-Grid-System/#forced-row)
* [Responsive Columns](https://brockenstein.github.io/Flexspan-Grid-System/#responsive-column)
* [Control the Gap](https://brockenstein.github.io/Flexspan-Grid-System/#gap)
* [Reverse Classes](https://brockenstein.github.io/Flexspan-Grid-System/#reverse)
* [Grid Alignment](https://brockenstein.github.io/Flexspan-Grid-System/#alignment)
* [Flex vs Forced Container](https://brockenstein.github.io/Flexspan-Grid-System/#fluid-forced)

# Team
## Main Contributors
* [Brock Barnett](https://github.com/Brockenstein) - Ideator, Lead Developer and Lead Documentation Writer
* [Donte White](https://github.com/dwhite02) - Developer, Tester and Documentation Writer
* [Malcom Harris](https://github.com/harrismalcolm) - Developer and Tester
* [Drew Hill](https://github.com/drewhilltmp) - Collaborator and Tester
* [Joe Sayegh](https://github.com/joesayegh) - Tester

## Special thanks to
* [Drew Toth](https://github.com/drew-git-tmp)
* [Paul Goepfert](https://github.com/pgoepfert)
* [Stephen Delancey](https://github.com/stephendelancey)
* [Laura Mahoney](https://github.com/lmahoney1218)
* [Josh Mahoney](https://github.com/jkmahoney)


## Inspiration
* [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid)
* [Flexbox Grid Mixins](https://github.com/thingsym/flexbox-grid-mixins)
