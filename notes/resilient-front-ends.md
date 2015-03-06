#Architecting resilient front ends

Andy Hume, Twitter (previously Clear Left and Guardian)

##When stuff goes wrong

Hundreds of thousands of dollars spent on colocation, database sharding etc.

But reliable front-ends are just as important. Unreliable networks can cause e.g. fonts not to load. And they are unrelaible. They slow down, drop out, get overloaded etc.

The web, however, is resilient. It ignores unknown CSS properties, sorts out badly formatted HTML and misses out undownloadbale images.

Progressive enhancement is the way we deal with this. It's as important to enhance for unreliable connections as well as underpowered browsers (e.g. work without JS because it hasn't loaded, not because they've turned it off)

##Three stages of priority

1. Content

2. Enhancement

3. Leftovers

Show people what they need first (e.g. news), then enhance it (e.g. carousels), then do other stuff (e.g. analytics)

**Time to screen is key**

Key performance metric: aim for 1s on mobile

Understand the network and the browser

##The network

DNS -> TCP -> HTTP request -> Server response -> HTTP response

Single threaded event loop.

The server esponse can be a redirect, which goes _right back to the start again_.

**Eliminate redirects**, flush the doc, prefetch DNS

##The browser

When the HTML gets bck to the browser, it:

* Constructs the DOM tree
* Constructs render tree from DOM and CSS
* Layout and paint

What can block it?

* Remote scripts stop, fetch and execute JS
* Inline scripts that rely on other downloaded content.
  (N.B. Scripts that write a new `script` tag don't get fetched by pre-parsers)
* Render tree is blocked by stylesheets
  Should we put essential CSS in the head?
* ...and fonts

##Blocking web fonts

It doesn't block the layout render, but it can block the text render.

IE just falls back to default font; Webkit and Opera (Blink) just fails; FF and Opera (Presto) blocks and then falls back. So use [Web font loader](https://github.com/typekit/webfontloader) to remove fonts from the critical path.

CSS fonts loading module is coming!

**Make pages that don't fail when one thing goes wrong**

Give users the best chance to use your product. Build resilience in!





