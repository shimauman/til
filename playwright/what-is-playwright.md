## Version
- Playwright requires Node.js v12 or above.

## Overview
- Node.js library.
- Provides cross-browser automation through a single API.
- Launches headless browsers by default.

### Terms
- cross-browser : ability of a website, HTML construct, application or even client-side script to work in several different environments, ones that provide its required features.
- headless browser : browser without UI.

## Sample Code
```js
// example.js

const playwright = require('playwright');

(async () => {
  const browser = await playwright.chromium.launch();
  const context = await browser.newContext();
  const page = await context.newPage();

  await page.goto('https://www.microsoft.com/edge');
  await page.screenshot({ path: 'example.png' });

  await browser.close();
})();
```
```
// We can get screenshot of Microsoft Edge top page.
$ node example.js
```

## Use Case
- Scraping Tool
- e2e test tool

## Reference
- [Microsoft docs : Use Playwright to automate and test in Microsoft Edge](https://docs.microsoft.com/en-us/microsoft-edge/playwright/)
