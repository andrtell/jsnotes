# Modules

```
$ tree

├── a.janet
├── b
│   └── init.janet
├── c
│   └── d.janet
└── main.janet
```

```janet
# a.janet

(def label "A")
```

```janet
# b/init.janet

(def label "B")
```

```janet
# c/d.janet

(def label "D")
```

```janet
# main.janet

(import ./a)
(import ./b)
(import ./c/d)

(defn main 
  [& args]
  (print a/label)
  (print b/label)
  (print d/label)
```

```sh
$ janet main.janet
A
B
D
```
