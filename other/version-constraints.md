## Version
- 

## Exact Version Constraint
- `1.0.1`

## Hyphenated Version Range
- `1.0 - 2.0` : 1.0.0 <= version < 2.1.0
- `1.0.0 - 2.1.0` : 1.0.0 <= version <= 2.1.0

## Wildcard Version Range
- `1.*` : 1.0.0 <= version < 2.0.0
- `1.0.*` : 1.0.0 <= version < 1.1.0

## Tilde Version Range
We can increase the number of latest digit.
- `~1.2` : 1.2.0 <= version < 2.0.0
- `~1.1.2` : 1.1.2 <= version < 1.2.0

## Caret Version Range
We fix the number(other than 0) of first digit.
- `^2.1.1` : 2.1.1 <= version < 3.0.0
- `^0.2.1` : 0.2.1 <= version < 0.3.0

## Reference
- [composer org docs : Writing Version Constraints](https://getcomposer.org/doc/articles/versions.md#writing-version-constraints)
