## Version
- 

## Sample
```html
<a href="javascript:void(0)" id="***" class="***">link</a>
```

## Caution
現在では推奨されていない。

- リンク先が`javascript:void(0);`と表示される。
- CSSのcursorを利用すればいい。

## Description
以下のようなジレンマを満たすための書き方。
- `a`タグを利用して、クリック可能であるとユーザーに認識させたい。
- `href`を設定しないとaタグは、リンクと見なさないことがある。
- `href`を設定すると、JavaScriptが動く前にリンク先に遷移する。
- `href`を設定したいけど、リンク先に飛ばさず、JavaScriptを動かしたい。

## What Is `void()`?
常に`undefined`(未定義であること示す値)を返すJavaScriptの演算子。

## Reference
- [MDN Web Docs : undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined)
- [MDN Web Docs : void operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/void)
