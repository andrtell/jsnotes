[Top](../javascript.md)

__Links__

MDN
> [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
>
> [structuredClone](https://developer.mozilla.org/en-US/docs/Web/API/Window/structuredClone)
>
> [get](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/get)
>
> [set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/set)

__Objects__

```javascript
// literal

let a = { x: 1 };

// constructed

let b = new Object()
b.x = 1;

// property access

a.x;

// key access

a["x"];

// bad name

a.z; // -> undefined

// computed name

let c = {
  ["a" + "b"]: 12
}

c.ab; // -> 12

// getters & setters

let d = {
  q: [1, 2],

  get peek() {
    return this.q[this.q.length - 1];
  },

  set top(v) {
    this.q.push(v);
  },
};

d.peek; // -> 2

d.top = 3

d.peek; // -> 3

```

Shallow copy

```javascript
let a = { x : 1 }

let b = { y : 2 }

{ ...a, ... b} // spread operator

Object.assign({}, a , b)
```

Deep copy

```javascript
let a = { x : 1 };

let b = { a: a };

structuredClone(b);
```
