[Top](../janet.md)

# Install Janet

```sh
$ git clone https://github.com/janet-lang/janet.git
```

```sh
$ cd janet
```

## Root-install

```sh
$ make -j
```

```sh
$ make test
```

```sh
$ sudo make install
```

```sh
$ sudo make install-jpm-git
```

## User-install

```
$ export PREFIX=$HOME/janet # (or some other dir)
```

```sh
$ make -j
```

```sh
$ make test
```

```sh
$ make install
```

```sh
$ make install-jpm-git
```
