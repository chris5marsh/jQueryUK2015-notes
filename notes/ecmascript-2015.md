#ECMAScript 2015

Dave Methvin, jQUery Foundation

Maintain and support jQuery products, plus others like Globalize, PEP, Esprima JS Parser

Javascript is just a trademarked form of ECMAScript

TC-39 is a committe made up of Moz, Apple, Google, MS, plus jQuery foundation (and others)

Like HTML, versioning is changing. ECMAScript 3 (1999), ES4 (abandoned), ES5 (2009), ES6 "Harmony" is almost done, but will just be ES 2015. It's a long process to release a whole new major release, so instead they will be releasing features as and when they are ready.

ES RC1 was released on Feb 20 2015.

##Two new kinds of features

  Things that can be polyfilled (e.g. `Map`, `Set`)
  Things that will make your browser choke (must be transpiled, e.g. Classes, Modules, etc.)

###Transpilers

Babel, supported by jsbin.com
Traceur
+ others

Grunt and Gulp plugins to transpile on build

##Some fun things

###`let` and `const`

####`let`

Declaring a variable with limited scope.

####`const`

Declaring non-variables that can't be changed. e.g. in a `for` loop so each elem in an array is set as a const. If you try to reassign the `const` it throws an error. But you can reassign properties of the `const`.

####The "Temporal Dead Zone"

Sounds awesome.

If you try and reference a `let` or a `const` in the block before it's defined it throws a ReferenceError. i.e. they are not hoisted.

####Tips

1. Use `const` by default
2. Use `let` if you have to rebind a variable
3. Use `var` to show it's ES5 code

###Destructuring

Allows you to assign multiple variable names to e.g. JSON passed in to a function. You can set default values, change the names of the variables.

You can swap variables:

```js
[x,y] = [y,x]
```

You can set default argument values!

###Template Strings

Multiple line string declarations within backticks. No more `"This is a "+thing`. You can use ${thing}.

##Compatibility

Still not widely supported in browsers, but you can use a transpiler like _Babel_ to process your ES6 code.

jsbin.com and babeljs.io/repl can use Babel to show you transpiled code.



