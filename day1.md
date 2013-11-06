# Day 1

## YUI AND THE FUTURE by Eric Ferraiuolo

A look at where the Web Platform is heading and how YUI fits into that future and continues to help you build web apps that run on many devices.

### What is YUI?

* a set of design principles
* infrastructure
* code organization
* abstraction
* loading

### The web platform

#### The Past
* Desktop browsers
* Basic HTML/CSS, JavaScript

#### Current
* HTML5/CSS3
* HTML/CSS
* JavaScript (ES5)
* JavaScript (ES3)
* Mobile
* Desktop

#### The Future
* Javascript (ES6)
* Web Components

#### ES6
* Proxies
* Modules
* let
* promises
* sets
* maps
* generators
* iterators
* =>
* class

#### Web Components
* Templates
* Decorators
* Custom Elements
* shadow DOM
* imports

#### Evergreen Browsers
Install once, update new stuff all the time. Big change. Used to browsers with long release cycles.

### The Web Platform + YUI
The role of YUI, or any framework, lib, polyfill, etc. is to fill in the gaps and smooth out the curve so we can write these long living applications.

### YUI + ES6 Modules
ES6 modules are defining a new syntax to declaritively import from other modules and export.

The goal is to use tooling to transpile modules into es6 modules. allows for backwards compatability.


## THE STATE OF GESTURES by Tilo Mitra

This talk is a technical deep dive into the world of gesture events. I'll introduce the work that has been and is currently being done in YUI Gestures and how you can use gesture events to create user experiences for mouse/touch and devices that support both.

### Challenges of multi-device user experiences

#### Evolving world of inputs

Primarily people used to interact with your site with a mouse.
Now we have touch devices, accelerometer, gyroscope, etc.
Recently we have had devices coming through that has mouse + touch.

This complicates things.

### Decouple events from inputs

What the [pointer spec](http://www.w3.org/TR/pointerevents/) is all about.

Pollyfill? nah improve the `gesturemove` events.

No matter what event comes in: 
* touch
* mouse
* MSPointer

fire a `geaturemove` event.

Higher level events that are built on top of `gesturemove` events:
* tap
* flick
* move/drag

`flick` is getting `flickup`, `flickleft`, etc. payload is direction velocity.

`geaturemovestart` is getting direction, `deltaX`, `deltaY`.


