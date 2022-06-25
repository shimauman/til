## Version
- 

## Best Practice
In e2e test with cypress, recommended locator is `data-cy` to **be isolated from all changes.**

```html
<button id="main" class="btn btn-large" name="submission" role="button" data-cy="submit">
    Submit
</button>
```
```js
cy.get('[data-cy=submit]').click()
```

## Summary Table
The import thing is the possibility to change the element in our future.
Selector | Recommended | Notes
-- | -- | --
`cy.get('button').click()` | Never | Worst - too generic, no context.
`cy.get('.btn.btn-large').click()` |  Never | Bad. Coupled to styling. Highly subject to change.
`cy.get('#main').click()` | Sparingly | Better. But still coupled to styling or JS event listeners.
`cy.get('[name="submission"]').click()` | Sparingly | Coupled to the name attribute which has HTML semantics.
`cy.contains('Submit').click()` | Depends | Much better. But still coupled to text content that may change.
`cy.get('[data-cy="submit"]').click()` | Always | Best. Isolated from all changes.

## Reference
- [](https://docs.cypress.io/guides/references/best-practices.html#Selecting-Elements)
