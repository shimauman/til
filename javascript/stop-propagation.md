## Version
- 

## Stop Propagation

When event occurs in html, the event is propagated on parent elements.
So, when we do not have to propagate the event, we have to write this.

```js
event.stopPropagation()
```

## Stop Immediate Propagation

When we add some event listeners on same target and event, we can stop other event listener which have not been called.

```js
event.stopImmediatePropagation()
```

## Reference
- [MDN Web Docs : stopPropagation](https://developer.mozilla.org/ja/docs/Web/API/Event/stopPropagation)
- [MDN Web Docs : stopImmediatePropagation](https://developer.mozilla.org/ja/docs/Web/API/Event/stopImmediatePropagation)
