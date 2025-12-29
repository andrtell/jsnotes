[Top](../javascript.md)

__Links__

MDN
> [Iterators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_generators)

# Iterators

```javascript
let a = {
  times: 3,

  next() {
    if (this.times--) {
      return {value: 7, done: false};
    }
    return {done: true};
  },

  [Symbol.iterator]() {
    return this; // iterate once.
  }
}

let v = [];

for (const x of a) {
  v.push(x)
}

v; // -> [7, 7, 7]
```
