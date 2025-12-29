[Top](../javascript.md)

__Links__

MDN
> [Iterators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_generators)
>
> [Iteration protocols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols)

# Iterators

```javascript
let a = {
  times: 3,

  // Iterator protocol

  next() { 
    if (this.times > 0) {
      return {value: this.times--, done: false};
    }
    return {done: true};
  },
  
  // Iterable

  [Symbol.iterator]() {
    return this;
  }
}

let v = [];

for (const x of a) {
  v.push(x)
}

v; // -> [3, 2, 1]
```
