#The cure for your Web Components hangover

Soledad Penade, Senior Engineer at Mozilla

One of the fastest talkers I've ever heard.

##Web components

Tectonic shift in web dev!

Make it easier to write modular, reusable code.

Side effects of Web 2.0 - bloated code, terrible code

**What if the browser helped us write better code?**

e.g. `<x-calendar></x-calendar>`

Web components is an umbrella term for custom elements, HTML templates, shadow DOM, HTML imports

##Custom Elements##

* Extends `HTMLElement.prototype`, attached to the DOM, methods and getters, setters
* Style custom elements in the same way as normal elements.
* Can extend from existing elements (e.g. make a new `button` type). This is good as it gives the browser a fallback element. (Might be deprecated soon...)

##HTML Templates

For example, adding rows to a table

##Shadow DOM

* Creates a boundary around your element
* Still in the same doc context
* Useful for things like calendars etc.
* A little like an `iframe`, but in same doc context

##HTML Imports

* Like `includes` for the web

Will be removed from Firefox, as there are concerns that it duplicates features (ES6 import,service workers...)

##Support

C,O everythng
FF: not HTML imports
Saf: --
IE: nothing

##Polyfills

They exist, but they come at a cost, e.g. shadow DOM polyfill is a beast.

Potential inconsistencies with HTML Imports

##Libraries

Polymner, XTag, Bosonic are syntactic sugar on top of Web Components. They allow you to extend WCs. But you need to include a whole library.

##How do they play with your frameworks

Should play nicely, as they are part of the DOM. jQuery plays well, as it's quite close to the DOM. The simpler your elements are, the better they will work. React sanitises some attributes. In Ember and Angular, they mostly work - can use custom elements in e.g. handlebars templates. But you can't use the `is=""` attribute. There is some weirdness though.

N.B. I don't use Ember or Angular, so a lot of this went over my head.

##Modularising your code is a good idea

We should be using components anyway! Don't tie your code to a specific framework. If you can afford to experiment, go for it!

e.g. Firefox OS refactored to use Web Components, Guardian reworked to use Web Components

Custom elements are the most usable now.

#Fail Safe Custom Elements

* Stay away from `is=""` markup
* Have a `.js` and `.css` per component
* Minimise your code
* Use the smallest polyfill
* Don't take anything for granted

As you start to refactor, your code will get leaner and more beatiful!




