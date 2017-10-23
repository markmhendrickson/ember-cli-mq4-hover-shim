# ember-cli-mq4-hover-shim

This is an Ember addon that ports [mq4-hover-shim](http://github.com/twbs/mq4-hover-shim) to automatically add class `hover` to the app layout's `html` tag when the app is initialized in browsers running on devices that properly support hover capabilities with their primary cursors.

It also integrates that shim's CSS preprocessor to convert instances of the hover media query into selectors based on that `html` tag class so browsers that don't support the hover media query can fall back to using those selectors.

This addon supports [FastBoot]() by checking for browser global variables before attempting to use them to determine contextual hover support. If any of those required global variables are unavailable (such as when the app is initialized in Node), this addon's initializer will trigger a console warning to that effect.

## Installation

Run `ember install ember-cli-mq4-hover-shim` within any Ember 2.0+ repository to install this addon.
