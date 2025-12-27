[Top](../javascript.md)

__Links__

MDN
> [<script>](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/script)

__Browser__

_Load_

Classic scripts can be loaded via the `<script>` tag.

```html
<script src="z.js"> 
```
```
                   ┌── JS download ──┬── JS execution ──┐                  
└── HTML parsing ──┘                                    └── HTML parsing ──┘
```

```html
<script defer src="z.js"> 
```

```
                          ┌── JS download ──┐           ┌── JS execution ──┐
└── HTML parsing ───────────────────────────────────────┘ 
```

```html
<script async src="z.js"> 
```

```
                    ┌── JS download ──┬── JS execution ──┐                  
└── HTML parsing ─────────────────────┘                  └── HTML parsing ──┘
```

_Scope_

Top-level names in classic scripts are made global (as properties on `window`).

```html
<script>
    var x = 1;
    function g(a) { console.log(a); }
</script>

<script>
    g(x); // ~> 1
    window.g(window.x); // ~> 1
</script>
```

