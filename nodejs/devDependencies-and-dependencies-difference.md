## Version
- 

```json
// package.json
{
  "name": "***",
  "version": "1.0.0",
  "description": "",
  "main": "***",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    ***
  },
  "dependencies": {
    ***
  }
}

```

## `dependencies` Packages
Which we use in the application.

```
// Add package in dependencies.
$ npm install package-name
or
$ npm i package-name
```

## `devDependencies` Packages
Which we use for development.

```
// Add package in devDependencies.
$ npm install package-name --save-dev
or
$ npm i package-name -D
```

## Why Divide
To improve production performance by removing unnecessary packages.

## Install Packages
On package.json directory,

```
// Install both of dependencies and devDependencies packages.
$ npm install
```
```
// Install only dependencies packages.
$ npm install --production
```

## Reference
- 
