## Version
- 

## How To Define
We can run workflow automatically when pull request events are occured.
```yml
// .github/workflows/sample.yml

on:
  pull_request: // To run by pull request events
    branches:
      - develop
      - main
    types: [opened, reopened, synchronize, closed]
```
When pull request whose target is `develop` or `main` branch is opened or reopened or synchronized or closed. we can run workflow automatically.
We have to set not default events in types.

## Pull Request Event List
- `assigned`
- `unassigned`
- `labeled`
- `unlabeled`
- `opened`(default)
- `edited`
- `closed`
- `reopened`(default)
- `synchronize`(default) : When we apply pushed commit into pull request.
- `ready_for_review`
- `locked`
- `unlocked`
- `review_requested`
- `review_request_removed`


## Reference
- [GitHub Docs : Events that trigger workflows - pull_request](https://docs.github.com/ja/actions/using-workflows/events-that-trigger-workflows#pull_request)
