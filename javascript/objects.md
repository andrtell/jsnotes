[Top](../javascript.md)

__Links__

MDN
> [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

__Javascript__

```html
<script type="module">

// literal
let a = { x: 1 } 

// constructed
let b = new Object() // -> {}
b.x = 1

typeof {} // -> "object"

typeof [] // -> "object"

let s = "abc";

typeof s; // -> "string"

typeof String(s); // -> "object"

s.length; // -> 3, s coerced into: new String(s)



</script>
