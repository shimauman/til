## Version
- Playwright v1.22

## Samples
```js
await page.locator('text=Log in').click();
await page.locator('Log in').click();
```
NOTE:
- `text=Log` does not match `<button>Log in</button>` because `<button>` contains a single text node "Log in" that is not equal to "Log".
- `text=Download` will not match `<button>download</button>`.
- Input elements of the type button and submit are matched by their value instead of text content. For example, text=Log in matches `<input type=button value="Log in">`.

<br>

```js
// Wrong, will match many elements including <body>
await page.locator(':has-text("Playwright")').click();

// Correct, only matches the <article> element
await page.locator('article:has-text("Playwright")').click();
```
NOTE: 
- The `:has-text()` pseudo-class can be used inside a css selector.
- `article:has-text("Playwright")` matches `<article><div>Playwright</div></article>`.

<br>

```js
await page.locator('#nav-bar :text("Home")').click();
```

NOTE:
- The `:text()` pseudo-class can be used inside a css selector
- It matches the smallest element containing specified text.

<br>

```js
await page.locator('#nav-bar :text-is("Home")').click();
```

NOTE:
- The `:text-is()` pseudo-class can be used inside a css selector, for strict text node match

<br>

```js
await page.locator('#nav-bar >> text=Contact Us').click();
```

<br>

```js
await page.locator('input:right-of(:text("Username"))').click();
```

<br>

```js
await page.locator(':nth-match(:text("Buy"), 3)').click();
```

<br>

```js
await page.locator('button', { hasText: 'Click me' }).click();
```
NOTE:
- Locators support an option to only select elements that have some text somewhere inside, possibly in a descendant element.


## Reference
- [playwright official docs : selectors](https://playwright.dev/docs/selectors)
