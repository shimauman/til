## Version
- 

## Sample
```html
<form>
  <div>
    <label>name</label>
    <input name="name" />
  </div>
  <button type="submit">Proceed</button>
</form>
```

## Keep The Subject
```js
cy.get('form') // yields <form>...</form>
  .contains('form', 'Proceed') // yields <form>...</form>
  .submit() // yields <form>...</form>
```

## No Keep
```js
cy.get('form') // yields <form>...</form>
  .contains('Proceed') // yields <button>...</button>
```

## Reference
- 
