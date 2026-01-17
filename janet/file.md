# Filesystem

```janet
(defn file-exists? [path]
  (not (nil? (os/stat path))))

```
