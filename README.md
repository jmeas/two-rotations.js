# two-rotations.js
[![Travis build status](http://img.shields.io/travis/jmeas/two-rotations.js.svg?style=flat)](https://travis-ci.org/jmeas/two-rotations.js)
[![Code Climate](https://codeclimate.com/github/jmeas/two-rotations.js/badges/gpa.svg)](https://codeclimate.com/github/jmeas/two-rotations.js)
[![Test Coverage](https://codeclimate.com/github/jmeas/two-rotations.js/badges/coverage.svg)](https://codeclimate.com/github/jmeas/two-rotations.js)
[![Dependency Status](https://david-dm.org/jmeas/two-rotations.js.svg)](https://david-dm.org/jmeas/two-rotations.js)
[![devDependency Status](https://david-dm.org/jmeas/two-rotations.js/dev-status.svg)](https://david-dm.org/jmeas/two-rotations.js#info=devDependencies)

A matrix for rotating vectors about two axes.

### Motivation

In three dimensions, there are three possible rotations – one about each axis. In many visualizations,
a combination of rotations about two axes is particularly important. This is because many visualizations
allow users to rotate the object about two axes by dragging the mouse.

#### Vectors

A vector is represented as a flat Javascript array of length 3. To define a vector, 

```js
var vector = [x, y, z];
```

In math lingo, this can be thought of as a column vector with dimensions `3x1`.

A point of confusion is that writing the array out like that makes it appear like a `1x3` row
vector. The relationship may be more clear if you think of the vector like so:

```js
var vector = [
  x,
  y,
  z
];
```

#### Usage

```js
// Define a vector
var vector = [1, 0, 0];

// Rotate the vector about some `pitch` and `yaw`
var newVector = twoRotations(vector, 20, 30);
```

#### API

###### `twoRotations( vector [, yaw] [, pitch] )

Rotate `vector` about a `yaw` angle, then a `pitch` angle. Angles are measured in radians.
