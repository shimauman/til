## Version
- Playwright v1.22

## Points
- The attributes will be changed rarely are what we have to use.
- For example, user-facing attributes like text content, input placeholder, accessibility roles and labels.
- If they will be changed frequently, we can use data-* attributes.
- It's better to avoid using long css or xpath chains because they have high possibility to be changed in feature.

## Good Samples
```js
await page.locator('text="Login"').click();
await page.locator('"Login"').click();

await page.locator('css=[placeholder="Search GitHub"]').fill('query');
await page.locator('[placeholder="Search GitHub"]').fill('query');

await page.locator('css=[aria-label="Close"]').click();
await page.locator('[aria-label="Close"]').click();

await page.locator('css=nav >> text=Login').click();
```
<br>

```html
<button data-test-id="directions">Itinéraire</button>
```
```js
await page.locator('css=[data-test-id=directions]').click();
await page.locator('[data-test-id=directions]').click();
await page.locator('data-test-id=directions').click();
```
NOTE:

Playwright supports the following attributes
- `id`
- `data-testid`
- `data-test-id`
- `data-test`

<br>

## Bad Samples
```js
await page.locator('#tsf > div:nth-child(2) > div.A8SBwf > div.RNNXgb > div > div.a4bIc > input').click();
await page.locator('//*[@id="tsf"]/div[2]/div[1]/div[1]/div/div[2]/input').click();
```

## Reference
- [playwright official docs : best practices](https://playwright.dev/docs/selectors#best-practices)
