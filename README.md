# WebGL Ball Throwing Game

My fun little prototype of a fairly simple WebGL game that uses a whole pile of new-fangle
tech like WebGL, Web Workers, Web Sockets, Pointer Lock and physics!

This thing is frankenstein'ed together from various examples, tidbits, blogs and github
repositories from far and wide. It's basically the culmination of things I've been poking at
for the last few years.

Art inspired by Tim Reynolds ([@turnislefthome](https://twitter.com/turnislefthome), http://www.turnislefthome.com)

Hope you enjoy, build upon, and hack this thing.

Btw, the code that's in this repo is a pile of garbage and contains various tangents and
ideas from the last year or two.

## Demo

Check it out: http://games.soarcetech.com/balls/


## Setup

1. Download or clone this repository
2. Install node.js (http://nodejs.org/) 
3. In the project root, install dependencies, e.g. `npm install`
4. Run the server: `node .`
5. Load up Google Chrome and visit `localhost:3000`

> You can specify a different port when running, e.g. `node . 8080`

Stop the server with CTRL+C

If you really want it to run and restart on crash, try this:

`while true; do echo 'Hit CTRL+C TO KILL'; node . ; sleep 1; done`

## Caveats

Since this is purely just a prototype of a game, there's absolutely no:

* **Performance**: movement is reported on a set interval, and is not optimal. Many clients in the server tends to flood the server out and lag everything out.
* **Security**: clients can hack and do naughty things
 * Clients handle their own balls, so clients report their own hits. 
* **Consistency**: physics are not synchronized on the server/clients. They could be, but this example lacks this for now. Check out Jonas Gehring's blog post on how this might be possible some day: http://www.jjoe64.com/2013/07/physijs-and-threejs-on-nodejs.html
 * Clients report the position and angle when firing balls. In theory, the ball will follow a pretty consistent path, but can vary a bit from client to client.

## Features

* HTML5, WebGL, Web Sockets, Web Workers, Pointer Lock
* HTML5 Boilerplate (http://html5boilerplate.com/)
* three.js (https://github.com/mrdoob/three.js/)
* physi.js (http://chandlerprall.github.io/Physijs/)
* node.js (http://nodejs.org/)

### Libraries and Misc
* THREE.PointerLockControls by Ricardo "mrdoob" Cabello (https://github.com/mrdoob/three.js/blob/master/examples/js/controls/PointerLockControls.js)
* Improved noise algorithm by Ken Perlin (http://mrl.nyu.edu/~perlin/noise/)
* GL Detector by AlteredQualia and Ricardo "mrdoob" Cabello (https://github.com/mrdoob/three.js/blob/master/examples/js/Detector.js)
* JavaScript Performance Monitor by Ricardo "mrdoob" Cabello (https://github.com/mrdoob/stats.js)
* jQuery Mousewheel by Brandon Aaron (http://brandonaaron.net)
* requestAnimationFrame polyfill by Erik Möller, Paul Irish and Tino Zijdel (http://paulirish.com/2011/requestanimationframe-for-smart-animating/)
* Shim for High Resolution Time by Tony Gentilcore (http://gent.ilcore.com/2012/06/better-timer-for-javascript.html)
* THREE.PlaneGeometry.js by Ricardo "mrdoob" Cabello (http://threejsdoc.appspot.com/doc/three.js/src.source/extras/geometries/PlaneGeometry.js.html)
* Keycode enum by Adam Vogel (http://adamvogel.net)
* Color sequence generator by Jim Bumgardner (http://krazydad.com/tutorials/makecolors.php)

## Credits

* Written by Kevin Fitzgerald ([@kftzg](https://twitter.com/kftzg), http://kevinfitzgerald.net)
* Art style inspired by Tim Reynolds ([@turnislefthome](https://twitter.com/turnislefthome), http://www.turnislefthome.com)
* Ideas vetted by bestie Adam Vogel ([@adambvogel](https://twitter.com/adambvogel), http://adamvogel.net)
* Play tested and approved by my lovely wife Luciana ([@leafitz](https://twitter.com/leafitz), http://lucianaelisa.net)
* Home grown in Milwaukee, WI
