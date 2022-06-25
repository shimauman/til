## Version
- 

## Sample
```html
<html>
  <body>
    <ul data-cy=fruit-list>
      <li>apples</li>
      <li>oranges</li>
      <li>bananas</li>
    </ul>
  </body>
</html>
```
```js
// yields <html>...<html>
cy.contains('apples');

// yields <ul>...</ul>
cy.contains('ul', 'apples');
cy.contains('[data-cy=fruit-list]', 'apples');
```

> Technically(理論上では、建前としては) the `html`, `body`, `ul`, and first `li` in the example above all contain “apples”. Normally Cypress would return the first `li` since that is the deepest element that contains “apples”. To override the element that is yielded we can pass `ul` or `[data-cy=fruit-list]` as the selector.

## Reference
- [Cypress docs : contains - Selector](https://docs.cypress.io/api/commands/contains.html#Selector)
