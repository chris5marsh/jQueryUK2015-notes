#Designing for displays that don't exist yet

Rosie Campbell, BBC R&D

Lots of different scopes of projects - some short term, some longer term, like designing for displays that don't exist.

##Evolution of displays

Everyone used to view web content on a small monitor, but browser support was difficult.

Now, displays are so different we _want_ different designs on different sizes.

Screens are getting weirder: watches, fridges, t-shirts...

##Don't panic!

###Case study: smart wallpaper

**What if you could paper the walls of your home with flexible, electronic wallpaper?**

Being ready for any new developments.

####Let user experience drive design, not the technology

* Take inspiration from sc-fi to create "design fiction"
* Have an "ideas amnesty" - no idea is a bad idea
* Take the most plausible forward to prototype

When TVs started being connected, web browsers didn't really work well on them. Now, Netflix etc. have redefined what's possible on a TV.

Mockups of most plausible types (kitchen wallpaper, study, kids' rooms).

#####Turn into an interactive prototype

* Frontend: HTML5, Canvas, JS
* Backend: NodeJS
* Fake with massive projector screens

Getting insights by mocking them up, feeding them back into how the technology is built. What's the best way to interact with the walls?

####Constraints breed creativity

Making assumptions can tease out novel ideas. e.g. it will probably be low power, low refresh. SO TV is still there for video, but smart wallpaper will augment the experience.


####Stay agnostic to underlying hardware

* Use standard web tech
* Most new devices will be internet-connected, so use web tech to deliver the service
* And you don't have to wait for the new tech to develop, you can apply it to any new tech that comes along

###What is responsive design?

Continuity between different contexts.

Rectangles are not enough! People have different shaped walls, fireplaces, sloped ceilings etc.

Can/should it be automated? People want control, but you don't want to position everything in your home!

Different types of content for different contexts (emails on your watch/phone, not on walls), children's content lower down etc.

People enjoy styling their home, so we need to replicate the user experience. And taking cues from computer science algorithms as well as user design.

##Summary

* Think UX first
* Use constraints to your advantage
* Hardware agnostic
