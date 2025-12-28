[Top](../javascript.md)

__Links__

MDN
> [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

__Objects__

```html
<script type="module">

// literal
let a = { x: 1 };

// constructed
let b = new Object() // -> {}
b.x = 1;

// property access
a.x;

// key access
a["x"];

// keys are always strings
a[7] = 9;

a["7"]; // -> 9

// computed property names
let c = {
  ["a" + "b"]: 12
}

c.ab; // -> 12

</script>
```
