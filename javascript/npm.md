[Top](../javascript.md)

__Links__

[NPM intro](https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager)

# NPM

```bash
$ npm init -y

$ ls
package.json

$ npm install express

$ ls
node_modules/ package.json package-lock.json

$ cat package.json
{
    "dependencies": {
        "express": "^5.2.1"
    }
}

$ npm install -D eslint

$ cat package.json
{
  "devDependencies": {
    "eslint": "^9.39.2"
  }
}

$ rm -rf node_modules

$ ls
package.json package-lock.json

$ npm install
added 148 packages, and audited 149 packages in 560ms

$ ls
node_modules/ package.json package-lock.json

$ npm update
up to date, audited 149 packages in 2s

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
