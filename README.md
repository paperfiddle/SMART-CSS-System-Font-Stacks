# SMART CSS System Font Stacks 

**Using `@font-face` + `local()` to build stacks with native system fonts.**

## Which fonts are we talking about? 

This project is about font stacks for rendering HTML in a web browser and includes:

* System UI fonts - the core OS fonts specific to on-screen reading and web browsing.
* Native system fonts - the fonts most common within a single OS.
* Websafe fonts - the fonts found on most devices.
* Default browser fonts - the generic `serif`, `sans-serif`, and `monospace` families. 

## The Method

As I was researching different approaches for building system font stacks, I immeadiatly loved Jonathan Neal's method mentioned on [CSS Tricks](https://css-tricks.com/snippets/css/system-font-stack/) with the [repository here](https://github.com/jonathantneal/system-font-css/blob/gh-pages/system-font.css).

If you've ever **self-hosted webfonts**, then you're familiar with the idea. For webfonts, you use `@font-face` to register a custom typeface name - like 'Lato 700i' - and it's sources.  The `src` always starts with a local source - like `local('Lato Bold Italic')`. This checks for cached or installed versions of the webfont before downloading it. For webfonts, the `src` will also contain either a data URI or URLs to the hosted files. 

For **system font stacks**, `@font-face` uses `local` to register a cascade of multiple native fonts under a single custom name that you can then use anywhere in your CSS. For exmple `System Sans 700i` would contain `local`s for the bold-italic typefaces of San Francisco, Segoe UI, Roboto, and so on. URIs and URLs are not used.  

For a stripped down example, [have a look at this CodePen](https://codepen.io/ljburton/pen/roQmGa?editors=1100) - it shows that you cannot get `bold` or `italic` from `local('Arial')` and demonstrates what to do instead. 

## Obtaining the correct `local` font names has been a complete PITA, so I thought I'd share :)

* Have a look at the [Wiki](https://github.com/paperfiddle/System-Font-Stacks/wiki) for the `local` names and usage notes for common system fonts. 
* Check out the SCSS for how I approach system font stacks. 
* Help improve the Wiki by contributing. 


