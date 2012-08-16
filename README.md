sun.js
======

Calculate sunrise and sunset times in Javascript.

This library extends the Javascript Date object, adding methods to calculate sunrise and sunset times. It also extends the Math object to add several useful support functions. If you don't like core JS types being extended you should probably rewrite this!

Based loosely and indirectly on Kevin Boone's SunTimes Java implementation of the US Naval Observatory's algorithm.

Usage is very simple:

```javascript

//Sunset tonight at the Triggertrap office
var sunset = new Date().sunset(51.4541, -2.5920);

//Sunrise at Stonehenge on midsummer's day 2000

var sunrise = new Date("2000-06-21").sunrise(51.1788, -1.8262);

//Combine it with geolocation. Sunset tonight at your location.

navigator.geolocation.getCurrentPosition(function(position) {
   	var sunset = new Date().sunset(position.coords.latitude, position.coords.longitude);
});

```

By Matt Kane (@ascorbic). Copyright © 2012 Triggertrap Ltd. All Rights Reserved.

This library is free software; you can redistribute it and/or modify it under the terms of the GNU Lesser General
Public License as published by the Free Software Foundation; either version 2.1 of the License, or (at your option)
any later version.
This library is distributed in the hope that it will be useful,but WITHOUT ANY WARRANTY; without even the implied
warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more
details.
You should have received a copy of the GNU Lesser General Public License along with this library; if not, write to
the Free Software Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301  USA,
or connect to: http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html

