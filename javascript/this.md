[Top](../javascript.md)

__Links__

MDN
> [this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

__This__

```html
<script type="module">
  function f() { return this; }

  f(); // => undefined (strict-mode)
</script>
```

```html
<script type="module">
  // ...
  f.call(7); // => 7
</script>
```
```html
<script type="module">
  // ...
  let obj = { f: f }
  obj.f(); // => { f: f }
</script>
```

