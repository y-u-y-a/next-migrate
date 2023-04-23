### How to publish package.

```shell:
$ npm login
$ npm publish
# Already published package name is cannot publish.

# Please command, if you want to remove package.
$ npm unpublish "package name"
```

### About package.json

```json:
{
  "name": "yuya-sample",
  "version": "0.0.4",
  "description": "",
  "type": "module", // "module" for "ECMAScript(import)", "commonjs" for "CommonJS(require)"
  "license": "MIT", // Commercial use permitted.
  "main": "dist/main.js", // Read when import.
  "types": "dist/main.d.ts", // For VSCode Completion.
  "files": [
    "dist"
  ],
  "repository": {
    "type": "git",
    "url": "https://github.com/y-u-y-a/next-migrate.git"
  },
  "author": "yuya",
  "contributors": [
    "yuya"
  ],
  //  User can search "npm search".
  "keywords": [
    "hello-world",
    "example"
  ],
  "peerDependencies": {},
  "devDependencies": {
    "typescript": "^4.0.0"
  },
  "scripts": {
    "build": "rm -rf dist && tsc src/*.ts --declaration --outDir dist",
    "prepublishOnly": "npm run build" // When "npm publish", run.
  }
}

```
