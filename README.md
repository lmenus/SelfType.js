# SelfType.js

JavaScript class that animates text similarly to the style that can be found at [Google Docs][google]' or [Slack][]'s homepage.

## Instructions

To use this library in your project, perform the following steps.

1. Copy the class SelfType into your project.
2. Tag the element whose contents should be animated with the `id="st-text"` attribute.
3. Add your own stylesheets (optional).
4. Start the animation by constructing a `var selftype = new SelfType()` class. You can optionally pass the constructor a configuration object. You can specify the following properties.
	```javascript

	{
        appendPeriod: boolean, // should a period be added after the animated text?
        backspace: boolean // should the text be removed one letter at a time?
        backspaceHighlight: boolean // should the text be highlighted before being deleted? (only if backspace is set to false)
        highlightColor: string // hexadecimal value of the colour to use for the highlight
		pause: integer // time in milliseconds on the end of animation,
		speed: 1 to 10, 'slow', 'normal', 'fast' // speed of the animation
        words: array // array of strings that will be animated on screen, min. length = 1
	}
	```
5. The library uses an interval to animate the text. This means that you'll have to remove it to prevent memory leaks. You can do so with `selftype.pause()`.
6. The object constructed with `new SelfType()` provides you with the following methods that can be used or modified at any time during the runtime.
    ```javascript

    selftype.options - complete configuration object that can be changed at any time
    selftype.pause() - pause the animation
    selftype.play() - play the animation
    ```

That's it! Enjoy SelfType!

## Demo

You can view the demo on [CodePen].

[codepen]: http://codepen.io/lmenus/pen/eZOYXo "SelfType.js demo"
[google]: https://www.google.com/docs/about/ "Google Docs' About Page"
[slack]: http://slack.com "Slack's Homepage"