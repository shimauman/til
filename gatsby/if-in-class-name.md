## Version
- 

## Samples
```jsx
<div className={isClass1 ? 'class1' : 'class2'}>
  gatsby
</div>
```
```jsx
<div className={`class1 ${isClass2 ? 'class2' : 'class3'}`}>
  gatsby
</div>
```
```jsx
<div className={`class1 ${isClass2 ? 'class2' : ''}`}>
  gatsby
</div>
```

This below sample needs attention.
```jsx
<div className={`class1 ${isClass2 && 'class2'}`}>
  gatsby
</div>
```

↓ If `isClass2` is false...

```html
<div className="class1 false">
  gatsby
</div>
```

## Reference
- 