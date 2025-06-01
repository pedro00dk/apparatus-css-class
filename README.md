# @\_apparatus\_/css-class

[![bundle size](https://deno.bundlejs.com/?q=@_apparatus_/css-class&badge=detailed)](https://bundlejs.com/?q=@_apparatus_/css-class)

A tiny utility for conditionally joining CSS classes.

## Installation

```sh
npm install @_apparatus_/css-class
```

## Examples

```typescript
import { cx } from '@_apparatus_/css-class'

// join classes
cx('foo', 'bar') // => 'foo bar'

// filter non-string values
cx('foo', undefined, null, false, true, 0, 1, 2n, 'bar') // => 'foo        bar'

// handle arrays
cx(['foo', ['bar', ['baz']]]) // => 'foo bar baz'

// handle objects
cx({ foo: true, bar: false, baz: 1 }) // => 'foo baz'

// mix and match
cx(false && 'foo', ['bar', { baz: true, qux: 0 }]) // => 'bar baz'
```
