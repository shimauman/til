## Version
- log4js v6.5.2

## Basic Usage
```
$ npm install log4js
```
```js
const log4js = require('log4js');
const logger = log4js.getLogger();
logger.level = 'debug';
logger.debug('Debug messages');
```

## Change Log Level
```js
logger.level = 'debug';

// We can output these revel logs.
// logger.trace('trace');
// logger.debug('debug');
// logger.info('info');
// logger.warn('warn');
// logger.error('error');
// logger.fatal('fatal');
```
```js
logger.level = 'info';

// We can output these revel logs.
// logger.info('info');
// logger.warn('warn');
// logger.error('error');
// logger.fatal('fatal');
```

## Wrap In Class
```js
const log4js = require('log4js');
const logger = log4js.getLogger();
logger = 'info';

export default class Logger {
  static info(message) {
    logger.info(message);
  }
}
```
```js
const Logger = require('./logger');
Logger.info('Info message');
```

## Reference
- [npm docs : log4js-node](https://www.npmjs.com/package/log4js)
- [Developers IO : Node.jsでlog4jsを使ってログを出力する](https://dev.classmethod.jp/articles/node-js-log4js/)
