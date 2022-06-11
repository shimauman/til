## Version
- 

## Sample
sample.js
```jsx
import { IntlContextConsumer, changeLocale, useIntl } from "gatsby-plugin-intl"

const intl = useIntl()

***
<IntlContextConsumer>
  {({ languages, language: currentLocale }) =>
    languages.map(language => (
      currentLocale !== language && (
        <button
          key={language}
          onClick={() => changeLocale(language)}
        >
          {intl.formatMessage({ id: "language" })}
        </button>
      )
    ))
  }
</IntlContextConsumer>
***
```

intl/en.json
```json
{
  "language": "日本語",
}
```

intl/ja.json
```json
{
  "language": "English",
}
```

## Reference
- [gatsby-plugin-intl components](https://www.gatsbyjs.com/plugins/gatsby-plugin-intl/#components)
