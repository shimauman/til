## Version
- 

## How To
```
yarn add gatsby-plugin-intl
```

gatsby-config.js
```js
plugins: [
  ***,
  {
    resolve: `gatsby-plugin-intl`,
    options: {
      path: `${__dirname}/src/intl`,
      languages: [`en`, `ja`],
      defaultLanguage: `en`,
      redirect: false, // option to redirect to `/en` when connecting `/`
    }
  },
  ***
]
```
src/intl/en.json
```json
{
  "hello": "Hi!"
}

```
src/intl/ja.json
```json
{
  "hello": "こんにちは"
}
```
component js file
```js
import { useIntl } from "gatsby-plugin-intl"

const intl = useIntl()

<p>
  {intl.formatMessage({ id: "hello" })}
</p>
```
or
```js
import { FormattedMessage } from "gatsby-plugin-intl"

<p>
  <FormattedMessage id="hello" />
</p>
```

## Reference
- [gatsby-plugin-intl](https://www.gatsbyjs.com/plugins/gatsby-plugin-intl/)
