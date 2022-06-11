## Version
- 

## Best Practice
Sample1
```html
<a href="https://shimauman.netlify.app" target="_blank" rel="noreferrer">
  Shimauman Web Site
</a>
```
or

Sample2
```html
<a href="https://shimauman.netlify.app" target="_blank" rel="noopener noreferrer">
  Shimauman Web Site
</a>
```

- Regarding to sample1, setting `target="_blank"` on `<a>` now implicitly provides the same rel behavior as setting `rel="noopener"`. However, This depends on browser compatibility.
- `rel="noreferrer"` is for some browsers which don't support `rel="noopener"`.

## Background
These rel attributes are to avoid tabnabbing.
> 仮にあなたが参考になる良い記事を見つけて、自分のサイト内のページに target="_blank" でリンクを貼ったとする。しかし、もしその参考記事が悪意のある第作者によって作られたページだった場合、開かれた新規タブ側で、リンク元のあなたのページのURLを操作できてしまう。もし、リンク元のあなたのページが、大手ショッピングサイトなどを装ったフィッシングサイトのURLに書き換えられてしまったらどうか。あなたのページからユーザーが個人情報を誤って入力してしまい、「あなたのページでフィッシング被害にあった！」なんて責められてしまう可能性もある。

## Reference
- [a tag browser compatibility](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#browser_compatibility)
- [noopener](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/noopener)
- [noreferrer](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/noreferrer)
- [tabnabbing description](https://wwg.co.jp/blog/3807#an22)
