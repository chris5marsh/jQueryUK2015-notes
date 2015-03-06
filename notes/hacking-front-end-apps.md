#Hacking front-end apps

Alex Sexton, Stripe

The web has a lot in common with Texas. Texas had a problem with littering in 1985. Some people defended their right to litter! Slogans and fines didn't help. Makes 18-24 were the core litterers - "Bubbas in pickup trucks".

So "Don't mess with Texas" was started, and it worked. 72% decrease in litter.

With online security, telling people not to do it because they should is _not_ going to work.

Web developers, **not security experts**, are the core audience. But it's hard.

We can't make perfect websites, with no flaws at all.

##Content injection

e.g. injecting scripts into the page and sending keypresses etc.

e.g Samy computer worm hacked MySpace, Evercookie

Why can't we just detect malicious scripts? It can be written in too msny different ways (Whitespace attack)

##CSS Hacks

`:visited` link styles could tell your browser history

##Timing attacks

Security by inaccuracy - timers on websites were so bad that you couldn't do it

e.g. comparing strings, seeing how long it takes to fail, can hack passwords

##JSON-P

JSON-Pretty-Insecure - it just injects a script in to your page.

You should probably use CORS (http://enable-cors.org).

##Cross site request forgery

POST, PUT, DELETE actions e.g. Facebook like buttons

That's why you have tokens.

But it's not just script tags - if you use attr selectors you can send requests for background images and discover what the 'hidden' attributes are.

##Snooping via OCR

##So what do we block? Everything with CSP

By default, block everything, and open little holes to get access to specific services.

Disallow cross-domain, apart from a whitelist

##CSP2 is out soon

This allows you to sign your inline scripts that you want to allow.

##SRI - sub resource integrity

Protects you against people trying to inject their scripts.

##HTTPS Everywhere

**Security by default**

