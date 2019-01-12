# font-face-system-stack

I'm using system fonts in my theme's fallback styles - I may switch to them completely someday. As I was researching different approaches, I immeadiatly loved Jonathan Neal's method mentioned on [CSS Tricks](https://css-tricks.com/snippets/css/system-font-stack/) with the [repository here](https://github.com/jonathantneal/system-font-css/blob/gh-pages/system-font.css).

In a nutshell, you use `@font-face` + local('Typface') to build your stacks. To do this, you must create an `@font-face` for every weight + style you need and you have to supply the correct typeface name. To understand why, [have a look at this CodePen](https://codepen.io/ljburton/pen/roQmGa?editors=1100).

Obtaining the correct typeface names has been a complete PITA, so I thought I'd share :)



## Resources 

@link https://support.apple.com/en-us/HT206872
@link https://github.com/lionhylra/iOS-UIFont-Names
@link http://iosfonts.com/
@link https://developer.apple.com/fonts/

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

## Sans Serif

### !Arial

@link https://docs.microsoft.com/en-us/typography/font-list/arial

| W    | local |
|------|-------|
| 400  | local('Arial'), local('ArialMT'), |
| 400i | local('Arial Italic'), local('Arial-ItalicMT') |
| 700  | local('Arial Bold'), local('Arial-BoldMT'), |
| 700i | local('Arial Bold Italic'), local('Arial-BoldItalicMT'), |
| 900  | local('Arial Black'), |

### Arial Narrow

@link https://docs.microsoft.com/en-us/typography/font-list/arial-narrow

| W    | local |
|------|-------| 
| 400  | local('Arial Narrow'), |
| 400i | local('Arial Narrow Italic'), |
| 700  | local('Arial Narrow Bold'), |
| 700i | local('Arial Narrow Bold Italic'), |

### Cantarell - GNOME

@link

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

### Droid Sans - Android < 3.26 Honeycomb

| W    | local |
|------|-------|
| 400  | local('Droid Sans'), local('DroidSans'), |
| 400i | local('Droid Sans Italic'), local('DroidSansItalic'), |
| 700  | local('Droid Sans Bold'), local('DroidSans-Bold'), |
| 700i | local('Droid Sans Bold Italic'), local('DroidSans-BoldItalic'), |

### !Helvetica - Mac

| W    | local |
|------|-------|
| 300  | local('Helvetica Light'), local('Helvetica-Light'), |
| 300i | local('Helvetica Light Oblique'), local('Helvetica-LightOblique'), |
| 400  | local('Helvetica'), local('Helvetica'), |
| 400i | local('Helvetica Oblique'), local('Helvetica-Oblique'), |
| 700  | local('Helvetica Bold'), local('Helvetica-Bold'), |
| 700i | local('Helvetica Bold Oblique'), local('Helvetica-BoldOblique'), |

### Helvetica Neue - OS X 10.10 Yosemite +

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

### Fira Sans - Firefox OS

@link http://mozilla.github.io/Fira/

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

### Lucida Grande - OS X 10.9 Mavericks

| W    | local |
|------|-------|
| 400 | local('Lucida Grande'), |
| 700 | local('Lucida Grande Bold'), |

	
### Oxygen-Sans - KDE Linux

@link https://github.com/KDE/oxygen-fonts	

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

### Roboto - Android 4.0 Ice Cream Sandwich +

@link https://google-webfonts-helper.herokuapp.com/fonts/roboto?subsets=latin

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

### !San Francisco OS X 10.11 El Capitan + 

Text

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

Display

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

Rounded 

| W   | local |
|-----|-------|
| 100 | local('SanFranciscoRounded-Ultralight') |
| 100 | local('SanFranciscoRounded-Thin') | 
| 100 | local('SanFranciscoRounded-Light') | 
| 100 | local('SanFranciscoRounded-Regular') | 
| 100 | local('SanFranciscoRounded-Medium') |
| 100 | local('SanFranciscoRounded-Semibold') |
| 100 | local('SanFranciscoRounded-Bold') | 
| 100 | local('SanFranciscoRounded-Heavy') | 
| 100 | local('SanFranciscoRounded-Black') | 

### Sergoe UI - Windows Vista +

@link https://docs.microsoft.com/en-us/typography/font-list/segoe-ui

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

### Trebuchet MS

@link https://docs.microsoft.com/en-us/typography/font-list/trebuchet-ms

| W    | local |
|------|-------|
| 400  | local('Trebuchet MS'), local('TrebuchetMS'), |
| 400i | local('Trebuchet MS Italic'), local('TrebuchetMS-Italic'), |
| 700  | local('Trebuchet MS Bold'), local('TrebuchetMS-Bold'), |
| 700i | local('Trebuchet MS Bold Italic'), local('Trebuchet-BoldItalic'), |

### Ubuntu

@link

| W    | local |
|------|-------|
| 100  |   |
| 100i |   |
| 200  |   |
| 200i |   |
| 300  | local('Ubuntu Light'), |
| 300i |   |
| 400  | local('Ubuntu'), |
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

### Verdana

@link https://docs.microsoft.com/en-us/typography/font-list/verdana

| W    | local |
|------|-------|
| 400  | local('Verdana'), local('Verdana'), |
| 400i | local('Verdana Italic'), local('Verdana-Italic'), |
| 700  | local('Verdana Bold'), local('Verdana-Bold'), |
| 700i | local('Verdana Bold Italic'), local('Verdana-BoldItalic'), |


## Serif


## Monospace


## Emoji 