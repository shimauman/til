## Version
- 

## Sample

```js
const array = [1,2,3,4];

$.each(array, function(index, value) {
    console.log(index + ' : ' + value);
})
```

### Loop HTML Elements
```html
<ul class="list">
    <li>foo</li>
    <li>bar</li>
</ul>
```
```js
$('.list').each(function(index) {
    console.log(index + ' : ' + $(this).text());
});

$('.list').each(function() {
    console.log($(this).text());
});

$('.list').each(function(index, element) {
    console.log(index + ' : ' + $(element).text());
});
```

## Reference
- [jQuery日本語リファレンス : jQuery.each(object, callback)](http://semooh.jp/jquery/api/utilities/jQuery.each/object%2C+callback/)