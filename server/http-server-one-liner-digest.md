## Version
-

## Sample Commands

### Python With `SimpleHttpServer`
```
$ python -m SimpleHTTPServer

// If we change port number.
$ python -m SimpleHTTPServer 3000
```

### Python v3.x
```
$ python -m http.server 8000
```

### PHP
```
$ php -S localhost:8000

// If we access from other host.
$ php -S 0.0.0.0:8000
```

### Node.js With `http-server`
```
// We can also install this pacakge unglobally.
$ npm install -g http-server
```
```
// The default port is 8080
$ http-server -p 8000

// We can open Web browser automatically with o option.
$ http-server -p 8000 -o
```

### Node.js With `server`
```
// We can also install this pacakge unglobally.
$ npm install -g serve
```
```
// The default port is 5000.
$ serve -p 8000

// We can use password auth function.
$ SERVE_USER=shimauman SERVE_PASSWORD=zebrahead serve --ah
```

## After Open Web Browser

### 1.
```
sample-project
  - index.html
  - create.html
  - show.html
```

### 2.
```
// On sample-project directory.
$ python -m http.server 8000
```

### 3.
Go to localhost:8000.

### 4.
Go to localhost:8000/index.html


## Reference
- [Qiita : ワンライナーWebサーバを集めてみた](https://qiita.com/sudahiroshi/items/e74d61d939f18779970d#nodejshttp-server%E7%B7%A8)
