# Filesystem

```janet
(defn file-exists? [path]
  (not (nil? (os/stat path))))
```

```janet
(defn slurp-file [path]
  (try
    (with [fh (file/open path)]
      [:ok (file/read fh :all)])
    ([err fib]
      [:error err])))
```
