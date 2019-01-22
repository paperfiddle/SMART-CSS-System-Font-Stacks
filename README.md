# SMART CSS System Font Stacks 

I recently started developing my own WordPress theme. When I got to fonts, I had a few questions:

* **Should I be using system fonts as my primary fonts - and not just my fallbacks?** Yes - when you want your site to feel 'mative' or familiar. 
* **Which fonts do I have to pick from, and which ones should I skip?** Turns out there are way better options than the browser defaults. Bye, Arial & Helvetica and a few others I don't like!
* **What's the best way implement system fonts?** Here I was looking for a way that could be the starting point in any theme. I took a hard look at using `font-family` vs `@font-face`. Both work, but `font-family` is the one I prefer. 


## What's Here?

* [/fonts/](https://github.com/paperfiddle/SMART-CSS-System-Font-Stacks/tree/master/fonts) - `.ttf` files for system UI + other fonts. 
* [/method-01/](https://github.com/paperfiddle/SMART-CSS-System-Font-Stacks/tree/master/method-01) - The `font-family` method for system fonts. 
* [/method-02/](https://github.com/paperfiddle/SMART-CSS-System-Font-Stacks/tree/master/method-02) - The `@font-face` method for system fonts. 
* [Wiki](https://github.com/paperfiddle/SMART-CSS-System-Font-Stacks/wiki) - A roundup of the resources I used to arrive at my stacks. If you're using `@font-face`, the wiki has `local`s. 

## Which Fonts?

This project is about font stacks for rendering HTML in a web browser and includes: 

* System UI fonts specific to on-screen reading and web browsing - as opposed to those for rendering application interfaces, print materials, terminals or consoles, and so on. 
* Native system fonts - the fonts most common across multiple versions of a single OS.
* Websafe fonts - the fonts available to most OSs, devices, and browsers.
* The generic `serif`, `sans-serif`, and `monospace` families. 
* The `-apple-system` and `BlinkMacSystemFont` abstractions. 

## Which Font Variants?

Users have the option to select their own default fonts, download additional fonts, and block sites from downloading webfonts. 

This table represents the coverage you can reasonably get with most font families. For more details, here's a [table summarizing system font weights and styles](https://docs.google.com/spreadsheets/d/1QtiGWURc1j0RdP8qA7FVJCXTJroHzNGUJpwQuVKt2eg/edit?usp=sharing).

Note that `sans-serif` 300, 600, 900 aren't supported on Chrome OS or by the most common Linux fonts. 

| W    | sans        | serif        | mono        |
|------|-------------|--------------|-------------|
| 100  | na          | na           | na          |
| 100i | na          | na           | na          |
| 200  | na          | na           | na          |
| 200i | na          | na           | na          |
| 300  | 'Sans 300'  | na           | na          |
| 300i | 'Sans 300i' | na           | na          |
| 400  | 'Sans 400'  | 'Serif 400'  | 'Mono 400'  |
| 400i | 'Sans 400i' | 'Serif 400i' | 'Mono 400i' |
| 500  | na          | na           | na          |
| 500i | na          | na           | na          |
| 600  | 'Sans 600'  | na           | na          |
| 600i | 'Sans 600i' | na           | na          |
| 700  | 'Sans 700'  | 'Serif 700'  | 'Mono 700'  |
| 700i | 'Sans 700i' | 'Serif 700i' | 'Mono 700i' |
| 800  | na          | na           | na          |
| 800i | na          | na           | na          |
| 900  | 'Sans 900'  | na           | na          |
| 900i | 'Sans 900i' | na           | na          |


## The `font-family` Method

	// Globals look like this 
	$font-family__sans: '-apple-system', 'BlinkMacSystemFont', 'San Francisco', 'Helvetica Neue', 'Sego UI', 'Roboto', sans-serif,  'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';

	// Mixins might look like this
	@mixin sans-400($size) {
		font-family: $font-family__sans;
		font-style: normal;
		font-weight: 400;
		font-size: $size;
	}
	@mixin sans-400i($size) {
		font-family: $font-family__sans;
		font-style: italic;
		font-weight: 400;
		font-size: $size;
	}

	// Usage looks like this
	p {
		@include sans-400(1em);
	}


## The `@font-face` Method

	// @font-face looks like this
	@font-face {
		font-family: 'Sans 400';
		font-style: normal;
		font-weight: 400;
		font-stretch: normal;
		src: local('-apple-system'), local('BlinkMacSystemFont'),
			local('SanFranciscoText-Regular'),
			local('Helvetica Neue'), local('HelveticaNeue'),
			local('Segoe UI'),
			local('Roboto'), local('Roboto-Regular'),
			local('Verdana'),
			local(sans-serif); 
	}
	@font-face {
		font-family: 'Sans 400i';
		font-style: italic;
		font-weight: 400;
		font-stretch: normal;
		src: local('-apple-system'), local('BlinkMacSystemFont'),
			local('SanFranciscoText-RegularItalic'),
			local('Helvetica Neue Italic'), local('HelveticaNeue-Italic'),
			local('Segoe UI Italic'),
			local('Roboto Italic'), local('Roboto-Italic'),
			local('Verdana Italic'),
			local(sans-serif); 
	}

	// Usage looks like this
	p {
		font-family: 'Sans 400';
	}