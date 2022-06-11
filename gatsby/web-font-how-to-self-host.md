## Version
- Gatsby v4

## How To

```
$ yarn add @fontsource/dm-sans
```

gatsby-browser.js
```js
const dmSans = require("@fontsource/dm-sans/latin-400.css")
module.exports = dmSans
```
css file
```css
***
font-family: "DM Sans";
***
```

## Self-Host Benefit
> You can decrease your site’s loading time by self-hosting fonts, saving ~300 milliseconds on desktop to 1+ seconds on 3G connections.

## Reference
- [self-host google fonts with font source](https://www.gatsbyjs.com/docs/how-to/styling/using-web-fonts/#self-host-google-fonts-with-fontsource)
- [font source code](https://github.com/fontsource/fontsource/tree/main/packages)