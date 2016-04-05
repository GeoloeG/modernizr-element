[![Bower version](https://badge.fury.io/bo/modernizr-element.svg)](https://badge.fury.io/bo/modernizr-element)
[![Build Status](https://travis-ci.org/MeTaNoV/modernizr-element.svg?branch=master)](https://travis-ci.org/MeTaNoV/modernizr-element)
[![Dependency Status](https://gemnasium.com/MeTaNoV/modernizr-element.svg)](https://gemnasium.com/MeTaNoV/modernizr-element)

`<modernizr-element>` is feature detection element based on [modernizr](https://modernizr.com/).

## Demo

[https://metanov.github.io/modernizr-element/](https://metanov.github.io/modernizr-element/components/modernizr-element/demo/index.html)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install modernizr-element --save
```

## Generating your `modernizr-custom.js` file

In order for the element to provide its feature detection functionality, a javascript file named `modernizr-custom.js` need to be generated.
This file will include all the tests available for feature detection by the `modernizr-element`.
Once the file has been produced, you will need to copy the file in the same folder as the `modernizr-element.html`. (e.g. `path/to/bower_components/modernizr/`)

There are several ways to produce the `modernizr-custom.js` file:

1. Using the [Modernizr website](https://modernizr.com/download?setclasses) download feature.
2. Using `modernizr` in your gulp file:
```javascript
gulp.task('modernizr', function(cb) {
  var detects = [
    'adownload',
    'blobconstructor',
    'flash'
  ].join();

  var output = 'frontend/js/modernizr.custom.js';

  return exec('./node_modules/.bin/modernizr -f ' + detects + ' -d ' + output,
    cb
  );
});
```
3. Using the [`gulp-modernizr`](https://github.com/doctyper/gulp-modernizr)

## Usage

Import Custom Element:

```html
<link rel="import" href="bower_components/modernizr-element/modernizr-element.html">
```

And then use it:

```html
<modernizr-element geolocation="{{_geolocation}}"></modernizr-element>
<p>Feature geolocation is : {{_geolocation}}</p>
```

See the [Documentation](https://metanov.github.io/modernizr-element/) for more options.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT License](http://opensource.org/licenses/MIT) © Pascal Gula

[![Throughput Graph](https://graphs.waffle.io/MeTaNoV/modernizr-element/throughput.svg)](https://waffle.io/MeTaNoV/modernizr-element/metrics)

