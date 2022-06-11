## Version
- 

## If not use intl plugin
```jsx
import { Link } from "gatsby"

<Link to={`/`}>
  gatsby
</Link>
```

## If use intl plugin
```jsx
import { useIntl, Link } from "gatsby-plugin-intl"

const intl = useIntl()

<Link to={`/`}>
  {intl.formatMessage({ id: "gatsby" })}
</Link>
```

## Reference
- [gatsby-plugin-intl components](https://www.gatsbyjs.com/plugins/gatsby-plugin-intl/#components)
