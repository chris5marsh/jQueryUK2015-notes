#Bin your &lt;select>

Alice Bartlett, front-end dev at GDS

##Who are GDS?

Building digital public services

Built gov.uk, 12 million visitors per week

Transforming govt. services, putting users' needs at the centre.

Open, agile, multidisciplinary teams, doing lots of user research

This user research highlights gaps in understanding in the way users interact with services. Do they really use these features? Do people really use computers in the way we think?

The audience is the _whole UK population_: people who use internet at work; on public computers; just for Facebook.

Reading comprehension age is that of a nine-year old.

All users _need_ to be there - it's an essential task, to do and get back on with your life.

##User research

**Participant 1:** office worker, not confident with computers, taking part in research with her boyfriend (techy friend). Clicks on select, types value she wants, gives it focus, not selection.

**Participant 2:** age 70, trying to get carer's allowance. Lower technical literacy due to age and economic bracket. These are the people that you need to build for. Could not use select boxes for DoB. But he could use a text input.

* Users are unable to close the select
* Typing into the select
* Confusing focus and selected
* Trying to pinch zoom select options

**All could use a text input successfully**

**Do the hard work to make it simple**

Looking like paper forms makes it easier. Just using text boxes.

Other people have understood this: Jakob Nielsen, Luke Wroblewski.

They should be the UI of last resort.

##Alternatives

* Will a text input suffice? (title can be)
* Small number of discrete data, use radio buttons
* If there are too many options to list consecutively
* If users would know the answer if they saw it, but might not know to type it in

##What is good?

* Accessible c.f. Steve Faulkner's checklist for accessibility - keyboard focusable, expected operation, clear indication, label, role etc.

* Functional without JS?

* Functional in which browsers? (IE7+ for gov.uk)

These last two make it more resilient. If you break the Javascript, will it still work?

**Do the hard work to make it simple**

Building custom widgets is hard, but it makes it simple for users.

##gov.uk's solution

List of checkboxes: keyboard focusable, give ARIA roles and controls to it to show/hide the options.


