# File

```janet
# main.janet

(defn main
  [& args]
  (with [f (file/open "main.janet")]
    (print (file/read f :all))))
```

```
$ janet main.janet

# main.janet

(defn main
  [& args]
  (with [f (file/open "main.janet")]
    (print (:read f :all))))
```
