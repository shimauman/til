## Version
- 

## Event
Composer has some events during its execution process.

## Command Events
- `post-install-cmd` : Occurs after the install command has been executed with a lock file present.
- `post-root-package-install` : Occurs after the root package has been installed during the create-project command (but before its dependencies are installed).

## How To Define
```json
// composer.json

"scripts": {
    "post-install-cmd": [
      "*** command ***"
    ],
    "post-update-cmd": [
      "*** command ***"
    ],
},
```

## Reference
 - [Composer org doc : Command Events](https://getcomposer.org/doc/articles/scripts.md#command-events)
 - [Qiita : Composerコマンド定義](https://qiita.com/yousan/items/94d035a838297b4afb8f)
