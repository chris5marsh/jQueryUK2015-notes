#mdoular CSS

(You know, because he's [mdo](https://twitter.com/mdo))

A CSS talk at a JS conference?

##Simple Class Structure

Dashes to join class sections (e.g. btn-primary)
Simple, obvious class names

If you use simple `.tabs` and `.tab-link` you can use `tab` on a `ul` or a `nav`, your `tab-link`s in an `a` or a `li`.

##Identifiable classes

Avoid common keywords e.g. use `.btn` not `.button`, otherwise you'll never find it amongst the `button`s.

##Base classes & prefixes

Isolate common stuff

Can use modifiers

Avoid collisions with similar components

e.g `.text-danger` and `.btn-danger` is better than `.danger`

##Minimise overrides

* Avoid shorthand unless necessary (e.g. use `margin-top:20px;`, `margin-bottom:20px;` instead of `margin:20px 0;`)
* Rely on modifier classes
* Build for reuse

##Keep it CSS-y

* CSS isn't a programming language
* Preprocessing can cloud vision
* Stick to variables, nesting and mixins (extends can add 100s of lines) (and imports?)

* Add plenty of comments
* Minimise nesting (mostly used for increasing specificity, makes code more fragile)
  Good nesting - `:hover`, `:active`
  Bad nesting - `.parent { .child { .element & { ... } } }`

##Formatting matters

Use CSSComb, code formatters to make the code look the same no matter what.

e.g.

1 Positioning
2 Box model (display, float, width...)
3 Typography
4 Visuals
5 Misc (CSS3)

##Document guidelines

Style guide; design guidelines; pattern library

c.f. codeguide.co, wtfhtmlcss.com, primercss.io

##Embrace utility classes

Sigle purpose, immutable declarations

e.g. `.left {float:left;}`, `.text-danger { color:red; }`

**Doesn't this take the complexity out of the CSS and put it in the HTML?**

e.g. `[hidden] { display:none !important; }`

##Automate and track CSS

* Linters and validators
* Grunt and Gulp
* Stats and reporting

e.g. Fail if class is not used in any view

Goal should be to remove as much code as possible.

Get size, number of selectors. Use Parker to get number of colours, declarations, selectors, rules to see if the changes you've made have broken your CSS.

cssstats.com is also a good tool.

##In summary

* Simplicity conquers all.
* Focus on what's between the curly braces.
* Document and evolve guidelines.


