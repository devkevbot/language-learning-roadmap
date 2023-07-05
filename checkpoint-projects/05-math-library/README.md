# Project 5: Math Library

This project covers the following topics:

- Modules
- Testing
- Error handling
- Bit manipulation

## Instructions

### Part 1: Library Code

In Part 1, we're going to develop a few functions for
a math utility library.

There are several required functions that need to be
implemented. Here's the pseudocode for the function signatures:

#### `clamp`

```js
// Clamps restricts `value` to the range [min, max]
// If `value` is less than `min`, `min` is returned.
// If the `value` is greater than `max`, `max` is returned.
// Otherwise, `value` itself is returned
//
// `min` must always be less than `max` and the function
// should raise an error is this condition is violated.
function clamp(value: int, min: int, max: int): int | error
```

#### `isPosPowerOfTwo`

```js
// Returns `true` is `x` is a positive power of 2 and `false` otherwise.
// Constraint: `x` will always be >= 0
//
// Hint: a positive power of two is a non-zero number
// with a single '1' in its binary representation
function isPosPowerOfTwo(x: int): bool
```

#### `binarySearch`
```js
// Returns `true` if `needle` is contained in `haystack` and `false` otherwise.
// Constraint: `haystack` must be sorted
// Constraint: operates in logarithmic time.
//
// Hint: a binary search is able to eliminate half
// of the search space at each step.
function binarySearch(needle: int, haystack: []int): bool
```

### Part 2: Testing Code

Once you've completed writing the library code, create
tests to verify that your functions work.

The expected behaviour of each function is as follows:

#### `clamp`

| inputs | result |
| -- | -- |
| `clamp(3, 0, 5)` | `3` |
| `clamp(-3, 0, 5)` | `0` |
| `clamp(10, 0, 5)` | `5` |
| `clamp(<any>, 5, 0)` | error thrown |

#### `isPosPowerOfTwo`

| inputs | result |
| -- | -- |
| `isPosPowerOfTwo(0)` | `false` |
| `isPosPowerOfTwo(1)` | `true` |
| `isPosPowerOfTwo(2)` | `true` |
| `isPosPowerOfTwo(4)` | `true` |

#### `binarySearch`

| inputs | result |
| -- | -- |
| `binarySearch(5, [1,2,3,4,5])` | `true` |
| `binarySearch(1, [1,2,3,4,5])` | `true` |
| `binarySearch(3, [1,2,3,4,5])` | `true` |
| `binarySearch(7, [1,2,3,4,5])` | `false`|
