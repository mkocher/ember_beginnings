!SLIDE

!SLIDE

# Ember.js

!SLIDE left

## Who are we?

David J. Hamilton - The Believer

Matthew Kocher - The Skeptic

!SLIDE left

## Overview

* Starting from the ground up
* Team of 6 rails developers with jQuery/Backbone experience

Goal of the project is to take a fresh look at Vertical Response's ten years of success, and position the company for the next ten.  Building a real app, planning for real load levels, but willing to invest the time to use something which will make for a better user experience.

!SLIDE left

## Getting Started

Two day spike - try it out, wrap Jasmine around it.

Get bindings working in our own sandbox, explore view/template linking.  Write some Jasmine model specs.

Didn't understand Ember controllers vs Rails controllers

In parallel, starting a rails back end, omniauth, beginnings of a domain model.

!SLIDE left

## Ember Data

Seemed to be ___the way forward___ though not ___production ready™___. (we've got the first of many pull requests open already)

Different model - not request/response but synchronization.

API Being defined as we speak.  `Todo.Models.Item.find(1)` just started working last week.

!SLIDE left

## App structure

Examples online for the most part use globals and bind directly to the right instance.  This makes us throw up in our mouths a little bit.

Lacking a Rails 5 minute blog or J2EE pet store canonical app.

Slowly been ripping out every `Ember.Xyz.create({})` that we thought was right and replacing with `Ember.Xyz.extend({})`

!SLIDE left

## Testing with Jasmine

Mock the clock - The DOM is slow.  Ember batches DOM updates using a run loop.  Mock the clock, tick the clock.

`Ember.testing` not documented, seems to just replace `jasmine.Clock.tick(1)` with `Ember.run()`

Test Pollution

Write helper functions - For instance, render a view and attach to the test dom.

Test are slow - our view tests are > 90% of our suite time.

!SLIDE left

## Open questions

Do we have to write the ember data rails adapter?

Are controllers global?  When should they be instantiated?  When should they be destroyed?

Where are the apps?  Travis-ci.org has been useful, but it's a bit of a special case app.  Todo examples are not big enough to drive out reusable patterns.

!SLIDE left

## Open questions (continued)

Shelling out the jQuery - Yes, we know we can make things display conditionally based on view/controller state. This seems heavyweight for a drop down menu, can we just have Ember trigger jQuery code?

Contributing Upstream - How long does a pull request take?

!SLIDE left

## Conclusions

We like it.  The parts that are done are solid, but there are plenty of places where features you expect just aren't there or are undocumented.

Slides available at [http://bit.ly/emberjs](http://bit.ly/emberjs)