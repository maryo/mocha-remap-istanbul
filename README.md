mocha-remap-istanbul
====================

[Mocha](http://visionmedia.github.com/mocha/) reporter to generate coverage report of [istanbul](http://gotwarlost.github.com/istanbul/) instrumented code.
Supports coverage remapping by [remap-istanbul](http://github.com/SitePen/remap-istanbul).
More than just inspired by [mocha-istanbul](http://github.com/arikon/mocha-istanbul), thanks guys.

Usage
-----
1. Install `mocha` and `mocha-remap-istanbul`
2. Instrument your code using `istanbul`
3. Make your tests to use the instrumented code
4. Run `mocha` using `mocha-istanbul` as a reporter
5. Use the environment variable `ISTANBUL_REPORTERS` to specify a comma separated list of istanbul reports with optional path. By default `ISTANBUL_REPORTERS=text-summary,html`
6. Use the environment variable `REMAP_ISTANBUL_REPORTERS` to specify a comma separated list of istanbul reports with optional path. To make this work you need to specify JSON reporter inside `ISTANBUL_REPORTERS` environment variable.

Example
-------
```javascript
process.env.ISTANBUL_REPORTERS = 'json=coverage/coverage.json';
process.env.REMAP_ISTANBUL_REPORTERS = 'text-summary,lcovonly=coverage/lcov.info,html=coverage/html';
```
