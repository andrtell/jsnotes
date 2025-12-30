[Top](../javascript.md)

__Links__

[NPM intro](https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager)

# NPM

```sh
$ npm init -y

$ ls
package.json
```

```sh
$ npm install express

$ ls
node_modules/ package.json package-lock.json

$ cat package.json
{
    "dependencies": {
        "express": "^5.2.1"
    }
}
```

```sh
$ npm install -D eslint

$ cat package.json
{
  "devDependencies": {
    "eslint": "^9.39.2"
  }
}
```

```sh
$ rm -rf node_modules

$ ls
package.json package-lock.json

$ npm install
added 148 packages, and audited 149 packages in 560ms

$ ls
node_modules/ package.json package-lock.json
```

```sh
$ npm update
up to date, audited 149 packages in 2s
```

```sh
$ npm run greet
npm error Missing script: "greet"

$ cat package.json
{
  "scripts": {
    "greet": "echo Hello"
  }
}

$ npm run greet
Hello
```
