# @font-face System Font Stack

I'm using system fonts in my theme's fallback styles - I may switch to them completely someday. As I was researching different approaches, I immeadiatly loved Jonathan Neal's method mentioned on [CSS Tricks](https://css-tricks.com/snippets/css/system-font-stack/) with the [repository here](https://github.com/jonathantneal/system-font-css/blob/gh-pages/system-font.css).

In a nutshell, you use `@font-face` + local('Typface') to build your stacks. To do this, you must create an `@font-face` for every weight + style you need and you have to supply the correct typeface name. To understand why, [have a look at this CodePen](https://codepen.io/ljburton/pen/roQmGa?editors=1100).

Obtaining the correct typeface names has been a complete PITA, so I thought I'd share :)

## Resources 

Generally helpful stuff I scraped from.

* @link https://support.apple.com/en-us/HT206872
* @link https://github.com/lionhylra/iOS-UIFont-Names
* @link http://iosfonts.com/
* @link https://developer.apple.com/fonts/

## Apple Abstractions

| local | 
|-------|
| local('system-ui'), |
| local('-apple-system'), |
| local('BlinkMacSystemFont'), |
| local('-apple-system-body'),|
| local('-apple-system-headline'), |
| local('-apple-system-subheadline'), |
| local('-apple-system-caption1'), |
| local('-apple-system-caption2'), |
| local('-apple-system-footnote'), |
| local('-apple-system-short-body'), |
| local('-apple-system-short-headline'), |
| local('-apple-system-short-subheadline'), |
| local('-apple-system-short-caption1'), |
| local('-apple-system-short-footnote'), |
| local('-apple-system-tall-body'), |

## !San Francisco - OS X 10.11 El Capitan + 

Does SF have serif or mono?

* @link https://developer.apple.com/fonts/

SF Text (sans)

| W    | local |
|------|-------|
| 300  | local('SanFranciscoText-Light'), |
| 300i | local('SanFranciscoText-LightItalic'), |
| 400  | local('SanFranciscoText-Regular'), |
| 400i | local('SanFranciscoText-RegularItalic'), |
| 500  | local('SanFranciscoText-Medium'), |
| 500i | local('SanFranciscoText-MediumItalic'), |
| 700  | local('SanFranciscoText-Bold'), |
| 700i | local('SanFranciscoText-BoldItalic'), |
| 900  | local('SanFranciscoText-Heavy'), |
| 900i | local('SanFranciscoText-HeavyItalic'), |

SF Display (sans)

| W   | local |
|-----|-------|
| 100 | local('SanFranciscoDisplay-Ultralight'), |
| 200 | local('SanFranciscoDisplay-Thin'), |
| 300 | local('SanFranciscoDisplay-Light'), |
| 400 | local('SanFranciscoDisplay-Regular'), |
| 500 | local('SanFranciscoDisplay-Medium'), |
| 600 | local('SanFranciscoDisplay-Semibold'), |
| 700 | local('SanFranciscoDisplay-Bold'), |
| 800 | local('SanFranciscoDisplay-Heavy'), |
| 900 | local('SanFranciscoDisplay-Black'), |

SF Rounded (sans)

| W   | local |
|-----|-------|
| 100 | local('SanFranciscoRounded-Ultralight') |
| 200 | local('SanFranciscoRounded-Thin') | 
| 300 | local('SanFranciscoRounded-Light') | 
| 400 | local('SanFranciscoRounded-Regular') | 
| 500 | local('SanFranciscoRounded-Medium') |
| 600 | local('SanFranciscoRounded-Semibold') |
| 700 | local('SanFranciscoRounded-Bold') | 
| 800 | local('SanFranciscoRounded-Heavy') | 
| 900 | local('SanFranciscoRounded-Black') | 

SF Compact Text (sans)

| W    | local |
|------|-------|
| 300  |   |
| 300i |   |
| 400  |   |
| 400i |   |
| 500  |   |
| 500i |   |
| 700  |   |
| 700i |   |
| 900  |   |
| 900i |   |

SF Compact Dispaly (sans)

| W    | local |
|------|-------|
| 100  |   |
| 200  |   |
| 300  |   |
| 400  |   |
| 500  |   |
| 600  |   |
| 700  |   |
| 800  |   |
| 900  |   |

## Helvetica Neue - OS X 10.10 Yosemite +

| W    | local |
|------|-------|
| 100  | local('Helvetica Neue UltraLight'), local('HelveticaNeue-UltraLight'),  |
| 100i | local('Helvetica Neue UltraLight Italic'), local('HelveticaNeue-UltraLightItalic'), |
| 200  | local('Helvetica Neue Thin'), local('HelveticaNeue-Thin'), |
| 200i | local('Helvetica Neue Thin Italic'), local('HelveticaNeue-ThinItalic'), |
| 300  | local('Helvetica Neue Light'), local('HelveticaNeue-Light'), |
| 300i | local('Helvetica Neue Light Italic'), local('HelveticaNeue-LightItalic'), |
| 400  | local('Helvetica Neue'), local('HelveticaNeue'), |
| 400i | local('Helvetica Neue Italic'), local('HelveticaNeue-Italic'), |
| 500  | local('Helvetica Neue Medium'), local('HelveticaNeue-Medium'), |
| 500i | local('Helvetica Neue Medium Italic'), local('HelveticaNeue-MediumItalic'), |
| 700  | local('Helvetica Neue Bold'), local('HelveticaNeue-Bold'), |
| 700i | local('Helvetica Neue Bold Italic'), local('HelveticaNeue-BoldItalic'), |
| 800  | local('Helvetica Neue Condensed Bold'), local('HelveticaNeue-CondensedBold'), |	
| 900  | local('Helvetica Neue Condensed Black'), local('HelveticaNeue-CondensedBlack'), |

## Lucida - OS X 10.9 Mavericks

Lucida Grande (sans)

| W    | local |
|------|-------|
| 400 | local('Lucida Grande'), |
| 700 | local('Lucida Grande Bold'), |

## Segoe - Windows Vista +

* @link https://docs.microsoft.com/en-us/typography/font-list/segoe-ui

Segoe UI (sans)

| W    | local |
|------|-------|
| 100  | local('Segoe UI Light'), |
| 100i | local('Segoe UI Light Italic'), |
| 300  | local('Segoe UI Semilight'), |
| 300i | local('Segoe UI Semiight Italic'), |
| 400  | local('Segoe UI'), |
| 400i | local('Segoe UI Italic'), |
| 600  | local('Segoe UI Semibold'), |
| 600i | local('Segoe UI Semibold Italic'), |
| 700  | local('Segoe UI Bold'), | 
| 700i | local('Segoe UI Bold Italic'), | 
| 900  | local('Segoe UI Black'), |
| 900i | local('Segoe UI Black Italic'), |


## Fira - Firefox OS

* @link http://mozilla.github.io/Fira/

Fira Sans

| W    | local |
|------|-------|
| 100 | local('Fira Sans Hair'), |
| 200 | local('Fira Sans UltraLight'), |
| 300 | local('Fira Sans Light'), |
| 400 | local('Fira Sans Regular'), |
| 500 | local('Fira Sans Medium'), |
| 600 | local('Fira Sans SemiBold'), |
| 700 | local('Fira Sans Bold'), |
| 800 | local('Fira Sans ExtraBold'), |
| 900 | local('Fira Sans Heavy'), |

Fira Mono

| W | local |
|---|-------|
| 400 | local('Fira Mono Regular'), |
| 500 | local('Fira Mono Medium'), |
| 700 | local('Fira Mono Bold'), |

## Roboto - Android 4.0 Ice Cream Sandwich +

Roboto 

* @link
* @link https://google-webfonts-helper.herokuapp.com/fonts/roboto?subsets=latin

| W    | local |
|------|-------|
| 100  | local('Roboto Thin'), local('Roboto-Thin'), |
| 100i | local('Roboto Thin Italic'), local('Roboto-ThinItalic'), |
| 300  | local('Roboto Light'), local('Roboto-Light'), |
| 300i | local('Roboto Light Italic'), local('Roboto-LightItalic'), |
| 400  | local('Roboto'), local('Roboto-Regular'), |
| 400i | local('Roboto Italic'), local('Roboto-Italic'), |
| 500  | local('Roboto Medium'), local('Roboto-Medium'), |
| 500i | local('Roboto Medium Italic'), local('Roboto-MediumItalic'), |
| 700  | local('Roboto Bold'), local('Roboto-Bold'), |
| 700i | local('Roboto Bold Italic'), local('Roboto-BoldItalic'), |
| 900  | local('Roboto Black'), local('Roboto-Black'), |
| 900i | local('Roboto Black Italic'), local('Roboto-BlackItalic'), |

Roboto Condensed (sans)

* @link
* @link

Roboto Slab (serif)

* @link https://fonts.google.com/specimen/Roboto+Slab/
* @link https://google-webfonts-helper.herokuapp.com/fonts/roboto-slab

| W | local |
|---|-------|
| 100 | local('Roboto Slab Thin'), local('RobotoSlab-Thin'), |
| 300 | local('Roboto Slab Light'), local('RobotoSlab-Light'), |
| 400 | local('Roboto Slab Regular'), local('RobotoSlab-Regular'), |
| 700 | local('Roboto Slab Bold'), local('RobotoSlab-Bold'), |

Roboto Mono (mono)

* @link https://fonts.google.com/specimen/Roboto+Mono/
* @link https://google-webfonts-helper.herokuapp.com/fonts/roboto-mono

| W    | local |
|------|-------|
| 100  | local('Roboto Mono Thin'), local('RobotoMono-Thin'), |
| 100i | local('Roboto Mono Thin Italic'), local('RobotoMono-ThinItalic'), |
| 300  | local('Roboto Mono Light'), local('RobotoMono-Light'), |
| 300i | local('Roboto Mono Light Italic'), local('RobotoMono-LightItalic'), |
| 400  | local('Roboto Mono'), local('RobotoMono-Regular'), |
| 400i | local('Roboto Mono Italic'), local('RobotoMono-Italic'), |
| 500  | local('Roboto Mono Medium'), local('RobotoMono-Medium'), |
| 500i | local('Roboto Mono Medium Italic'), local('RobotoMono-MediumItalic'), |
| 700  | local('Roboto Mono Bold'), local('RobotoMono-Bold'), |
| 700i | local('Roboto Mono Bold Italic'), local('RobotoMono-BoldItalic'), |


## Droid - Android 3.26 Honeycomb <= 

* @link 

Droid Sans

| W    | local |
|------|-------|
| 400  | local('Droid Sans'), local('DroidSans'), |
| 400i | local('Droid Sans Italic'), local('DroidSansItalic'), |
| 700  | local('Droid Sans Bold'), local('DroidSans-Bold'), |
| 700i | local('Droid Sans Bold Italic'), local('DroidSans-BoldItalic'), |

Droid Serif 

| W | local |
|---|-------|
| 400  | local('Droid Serif'), local('DroidSerif'), |
| 400i | local('Droid Serif Italic'), local('DroidSerif-Italic'), |
| 700  | local('Droid Serif Bold'), local('DroidSerif-Bold'), |
| 700i | local('Droid Serif Bold Italic'), local('DroidSerif-BoldItalic'), |

Droid Sans Mono

| W | local |
|---|-------|
| 400  | local('Droid Sans Mono'), local('DroidSansMono'), |
| 400i |   |
| 700  |   |
| 700i |   |

## Oxygen  - KDE Linux

* @link https://github.com/KDE/oxygen-fonts	

Oxygen Sans

| W    | local |
|------|-------|
| 100  |   |
| 100i |   |
| 200  |   |
| 200i |   |
| 300  |   |
| 300i |   |
| 400  |   |
| 400i |   |
| 500  |   |
| 500i |   |
| 600  |   |
| 600i |   |
| 700  |   |
| 700i |   |
| 800  |   |
| 800i |   |
| 900  |   |
| 900i |   |

## Umbutu

* @link https://design.ubuntu.com/font/

Umbutu (sans)

* @link https://fonts.google.com/?query=Ubuntu
* @link https://google-webfonts-helper.herokuapp.com/fonts/ubuntu?subsets=latin

| W    | local |
|------|-------|
| 300  | local('Ubuntu Light'), local('Ubuntu-Light'), |
| 300i | local('Ubuntu Light Italic'), local('Ubuntu-LightItalic'), |
| 400  | local('Ubuntu Regular'), local('Ubuntu-Regular'), |
| 400i | local('Ubuntu Italic'), local('Ubuntu-Italic'), |
| 500  | local('Ubuntu Medium'), local('Ubuntu-Medium'), |
| 500i | local('Ubuntu Medium Italic'), local('Ubuntu-MediumItalic'), |
| 700  | local('Ubuntu Bold'), local('Ubuntu-Bold'), |
| 700i | local('Ubuntu Bold Italic'), local('Ubuntu-BoldItalic'), |

Ubuntu Condensed (serif)

* @link https://fonts.google.com/specimen/Ubuntu+Condensed
* @link https://google-webfonts-helper.herokuapp.com/fonts/ubuntu-condensed

| W    | local |
|------|-------|
| 400  | local('Ubuntu Condensed'), local('UbuntuCondensed-Regular'),|

Ubuntu Mono

* @link https://fonts.google.com/specimen/Ubuntu+Mono
* @link https://google-webfonts-helper.herokuapp.com/fonts/ubuntu-mono

| W    | local |
|------|-------|
| 400  | local('Ubuntu Mono'), local('UbuntuMono-Regular'), |
| 400i | local('Ubuntu Mono Italic'), local('UbuntuMono-Italic'), |
| 700  | local('Ubuntu Mono Bold'), local('UbuntuMono-Bold'), |
| 700i | local('Ubuntu Mono Bold Italic'), local('UbuntuMono-BoldItalic'), |

## Cantarell - GNOME

* @link

| W    | local |
|------|-------|
| 100  |   |
| 100i |   |
| 200  |   |
| 200i |   |
| 300  |   |
| 300i |   |
| 400  | local('Cantarell'), |
| 400i |   |
| 500  |   |
| 500i |   |
| 600  |   |
| 600i |   |
| 700  |   |
| 700i |   |
| 800  |   |
| 800i |   |
| 900  |   |
| 900i |   |	

## Emoji 

| local |
|-------|
| local('Apple Color Emoji'),|
| local('Segoe UI Emoji'),|
| local('Segoe UI Symbol'),|
| |




## Websafe Sans

!Arial

* @link https://docs.microsoft.com/en-us/typography/font-list/arial

| W    | local |
|------|-------|
| 400  | local('Arial'), local('ArialMT'), |
| 400i | local('Arial Italic'), local('Arial-ItalicMT') |
| 700  | local('Arial Bold'), local('Arial-BoldMT'), |
| 700i | local('Arial Bold Italic'), local('Arial-BoldItalicMT'), |
| 900  | local('Arial Black'), |

Arial Narrow

* @link https://docs.microsoft.com/en-us/typography/font-list/arial-narrow

| W    | local |
|------|-------| 
| 400  | local('Arial Narrow'), |
| 400i | local('Arial Narrow Italic'), |
| 700  | local('Arial Narrow Bold'), |
| 700i | local('Arial Narrow Bold Italic'), |


!Helvetica - Mac

| W    | local |
|------|-------|
| 300  | local('Helvetica Light'), local('Helvetica-Light'), |
| 300i | local('Helvetica Light Oblique'), local('Helvetica-LightOblique'), |
| 400  | local('Helvetica'), local('Helvetica'), |
| 400i | local('Helvetica Oblique'), local('Helvetica-Oblique'), |
| 700  | local('Helvetica Bold'), local('Helvetica-Bold'), |
| 700i | local('Helvetica Bold Oblique'), local('Helvetica-BoldOblique'), |

Trebuchet MS

* @link https://docs.microsoft.com/en-us/typography/font-list/trebuchet-ms

| W    | local |
|------|-------|
| 400  | local('Trebuchet MS'), local('TrebuchetMS'), |
| 400i | local('Trebuchet MS Italic'), local('TrebuchetMS-Italic'), |
| 700  | local('Trebuchet MS Bold'), local('TrebuchetMS-Bold'), |
| 700i | local('Trebuchet MS Bold Italic'), local('Trebuchet-BoldItalic'), |

Verdana

* @link https://docs.microsoft.com/en-us/typography/font-list/verdana

| W    | local |
|------|-------|
| 400  | local('Verdana'), local('Verdana'), |
| 400i | local('Verdana Italic'), local('Verdana-Italic'), |
| 700  | local('Verdana Bold'), local('Verdana-Bold'), |
| 700i | local('Verdana Bold Italic'), local('Verdana-BoldItalic'), |

## Websafe Serif

!Georgia - Windows + Mac

* @link

| W | local |
|---|-------|
| 400   | local('Georgia'),  |
| 400i  | local('Georgia Italic'), local('Georgia-Italic'), |
| 700   | local('Georgia Bold') local('Georgia-Bold'), |
| 700i  | local('Georgia Bold Italic') local('Georgia-BoldItalic'), |

## Websafe Mono

Courier 

* @link

| W | local |
|---|-------|
| 400  | local('Courier'), local('Courier'), |
| 400i | local('Courier Oblique'), local('Courier-Oblique'), |
| 700  | local('Courier Bold '), local('Courier-Bold'), |
| 700i | local('Courier Bold Oblique'), local('Courier-BoldOblique'), |

Courier New 

* @link

| W | local |
|---|-------|
| 400  | local('Courier New'), local('CourierNewPSMT), |
| 400i | local('Courier New Italic'), local('CourierNewPS-ItalicMT), |
| 700  | local('Courier New Bold'), local('CourierNewPS-BoldMT), |
| 700i | local('Courier New Bold Italic'), local('CourierNewPS-BoldItalicMT), |

























Consolas, 
'Andale Mono WT', 
'Andale Mono', 
'Lucida Console', 
'Lucida Sans Typewriter', 
'DejaVu Sans Mono', 
'Bitstream Vera Sans Mono', 
'Liberation Mono', 
'Nimbus Mono L', 
Monaco, 




| W | local |
|---|-------|
| 100  |   |
| 100i |   |
| 200  |   |
| 200i |   |
| 300  |   |
| 300i |   |
| 400  |   |
| 400i |   |
| 500  |   |
| 500i |   |
| 600  |   |
| 600i |   |
| 700  |   |
| 700i |   |
| 800  |   |
| 800i |   |
| 900  |   |
| 900i |   |