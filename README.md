# plucker [![Flattr this!](https://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=hughskennedy&url=http://github.com/hughsk/plucker&title=plucker&description=hughsk/plucker%20on%20GitHub&language=en_GB&tags=flattr,github,javascript&category=software)[![experimental](http://hughsk.github.io/stability-badges/dist/experimental.svg)](http://github.com/hughsk/stability-badges) #
[![plucker](https://nodei.co/npm/plucker.png?mini=true)](https://nodei.co/npm/plucker)

Pluck nested properties from an object.

## Usage
```js
const plucker = require('plucker')

const pluck = plucker('foo.bar')
pluck({ foo: { bar: 'hello' } })
// => 'hello'
```

## API ##


### pluck = plucker(path) ###

Given a dot-delimted property `path`, returns a plucking function.

You can also pass in an array of string keys, in case you want to avoid
splitting a key which is intended to have dots in it.

### pluck(object) ###

Pass this function an object to pluck the nested value from it.

To pluck values from an array, you can simply use it with `[].map`, like so:

``` javascript
var pluck = require('plucker')
var array = require('./data.json')

return array.map(
  pluck('some.nested.value')
)
```

### plucker(path, object) ###

Shorthand for `plucker(path)(object)`.

## See Also
- [flat](https://github.com/hughsk/flat) - Flatten/unflatten nested Javascript
  objects

## License ##

MIT. See [LICENSE.md](http://github.com/hughsk/plucker/blob/master/LICENSE.md) for details.
