## Version
- PurgeCSS v1.4.0 and above

## What Is Purging Tailwind CSS
> Now we’ve fully configured Tailwind CSS, we want to make sure that only the classes we need are delivered to the browser. By default, Tailwind is a very large library because it includes every combination of every class you might think of. Most of these you won’t need, so we use PurgeCSS to remove any unused classes.

## How To
tailwind.config.js

```js
module.exports = {
  purge: ["./src/**/*.{js,jsx,ts,tsx}"],
  theme: {},
  variants: {},
  plugins: [],
}
```

## Reference
- [tailwind css purging your css](https://www.gatsbyjs.com/docs/how-to/styling/tailwind-css/#4-purging-your-css)
