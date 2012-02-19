# Platform.js

A platform detection library that works on nearly all JavaScript platforms<sup><a name="fnref1" href="#fn1">1</a></sup>.

## Disclaimer

Platform.js is for informational purposes only and **not** intended as a substitution for [feature detection/inference](http://www.screenr.com/5Ab) checks.

## BestieJS

Platform.js is part of the BestieJS *"Best in Class"* module collection. This means we promote solid browser/environment support, ES5 precedents, unit testing, and plenty of documentation.

## Documentation

The documentation for Platform.js can be viewed here: [/doc/README.md](https://github.com/bestiejs/platform.js/blob/master/doc/README.md#readme)

For a list of upcoming features, check out our [roadmap](https://github.com/bestiejs/platform.js/wiki/Roadmap).

## Installation and usage

In a browser or Adobe AIR:

~~~ html
<script src="platform.js"></script>
~~~

Via [npm](http://npmjs.org/):

~~~ bash
npm install platform
~~~

In [Narwhal](http://narwhaljs.org/), [Node.js](http://nodejs.org/), and [RingoJS](http://ringojs.org/):

~~~ js
var platform = require('platform');
~~~

In [Rhino](http://www.mozilla.org/rhino/):

~~~ js
load('platform.js');
~~~

In [RequireJS](http://requirejs.org/):

~~~ js
require({
  'paths': {
    'platform': 'path/to/platform'
  }
},
['platform'], function(platform) {
  console.log(platform.name);
});
~~~

Usage example:

~~~ js
// on IE10 x86 platform preview running in IE7 compatibility mode on Windows 7 64 bit edition
platform.name; // 'IE'
platform.version; // '10.0'
platform.layout; // 'Trident'
platform.os; // 'Windows Server 2008 R2 / 7 x64'
platform.description; // 'IE 10.0 x86 (platform preview; running in IE 7 mode) on Windows Server 2008 R2 / 7 x64'

// or on an iPad
platform.name; // 'Safari'
platform.version; // '5.1'
platform.product; // 'iPad'
platform.manufacturer; // 'Apple'
platform.layout; // 'WebKit'
platform.os; // 'iOS 5.0'
platform.description; // 'Safari 5.1 on Apple iPad (iOS 5.0)'

// or parsing a given UA string
var info = platform.parse('Mozilla/5.0 (Macintosh; Intel Mac OS X 10.7.2; en; rv:2.0) Gecko/20100101 Firefox/4.0 Opera 11.52');
info.name; // 'Opera'
info.version; // '11.52'
info.layout; // 'Presto'
info.os; // 'Mac OS X 10.7.2'
info.description; // 'Opera 11.52 (identifying as Firefox 4.0) on Mac OS X 10.7.2'
~~~

## Cloning this repo

To clone this repository including all submodules, using Git 1.6.5 or later:

~~~ bash
git clone --recursive https://github.com/bestiejs/platform.js.git
cd platform.js
~~~

For older Git versions, just use:

~~~ bash
git clone https://github.com/bestiejs/platform.js.git
cd platform.js
git submodule update --init
~~~

Feel free to fork if you see possible improvements!

## Footnotes

  1. Platform.js has been tested in at least Adobe AIR 2.6, Chrome 5-15, Firefox 1.5-8, IE 6-10, Opera 9.25-11.52, Safari 2-5.1.1, Node.js 0.4.8-0.6.1, Narwhal 0.3.2, RingoJS 0.7-0.8, and Rhino 1.7RC3.
     <a name="fn1" title="Jump back to footnote 1 in the text." href="#fnref1">&#8617;</a>

## Authors

* [John-David Dalton](http://allyoucanleet.com/)
  [![twitter/jdalton](http://gravatar.com/avatar/299a3d891ff1920b69c364d061007043?s=70)](https://twitter.com/jdalton "Follow @jdalton on Twitter")

## Contributors

* [Mathias Bynens](http://mathiasbynens.be/)
  [![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](https://twitter.com/mathias "Follow @mathias on Twitter")