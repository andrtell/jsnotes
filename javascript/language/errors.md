[Top](../../javascript.md)

__Links__

MDN
> [Error handling](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling)
> 
> [Error types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error#error_types)

# Errors

```javascript
try {
  throw new Error():
} catch {
  // ...
}
```

```javascript
try {
  throw Error("123");
} catch(e) {
  e.name;    // "Error" 
  e.message; // "123" 
}
```

```javascript
try { 
  throw Error(); 
} catch (e) { 
  throw e; // re-throw
}
```

```javascript
try {
  // ...
} catch (e) {
  if (e instanceof RangeError) {
    // ...
  } else {
    throw e;
  }
}
```

```javascript
try {
  throw Error();
} catch (e) {
  throw e;
} finally {
  // ...
}
```

```javascript
try {
  try {
    throw new Error();
  } finally {
    // 1
  }
} catch {
  // 2
}
```

```javascript
function f() {
  try {
    throw Error();
  } finally {
    return 1;
  }
}

f(); // 1

```
