[Top](../javascript.md)

__Links__

MDN
> [Promise()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/Promise)

# Promises

`new Promise()` is primarily used to wrap callback-based APIs that do not already support promises.

```javascript
const f = setTimeout, g = setTimeout;
```

```javascript
f(
  function cb() {
    g(
      function cb() {
        // ...
      }
    )
  }
);
```

```javascript
let p = new Promise( // p is 'pending'.
  function executor(resolve) { // called synchronously.
    f(
      function cb() {
        g(
          function cb() {
            // p becomes 'fulfilled' when resolve() is given a non-promise (implicit 'undefined' here).
            resolve();     
          }
        )
      }
    );
  }
);

p.then(
  // queued up synchronously, called when p is 'fulfilled'.
  function ok() {
    console.log('p is fulfilled');
  }
)

// p is fulfilled
```

```javascript
let q = new Promise(
  function executor(resolve) {
    f(
      function cb() {
        r = new Promise(
          function executor(resolve) {
            g(
              function cb() {
                // r becomes 'fulfilled'.     
                resolve(); 
              }
            )    
          }
        )

        r.then(function ok() { console.log('r is fulfilled'); })

        // q remains 'pending'. q's faith is now tied to that of r.
        resolve(r);   
      }
    );
  }
);

q.then(function ok() { console.log('q is fulfilled'); })

// r is fulfilled
// q is fulfilled
```



```javascript
let q = new Promise(
  function executor(resolve) {
    f(resolve);
  }
);

q.then( 
  function () {
    let r = new Promise(
      function executor(resolve) {
        g(resolve);
      }
    );

    r.then( // nested .then(), here for completeness.
      function() {
        // ...
      }
    )
  }
)

```

```javascript
let u = new Promise(
  function executor(resolve) {
    f(resolve);
  }
);

let w = u.then(
  function () {
    let v = new Promise(
      function executor(resolve) {
        g(resolve);
      }
    );

    return v;
  }
)

w.then(
  function () {
    // ...
  }
);
```

```javascript
let a = function () {
  return new Promise(function executor(resolve) { f(resolve); });
}

let b = function () {
  return new Promise(function executor(resolve) { g(resolve); });
}
```

```javascript
a().then(
  function() {
    return b();
  }
).then(
  function() {
    // ...
  }
);
```

```javascript
a().then(b).then(function () { /* ... */ });
```

```javascript
await a();
await b();

// ...
```
