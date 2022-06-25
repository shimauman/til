## Version
- 

## How To Define
```yml
// .github/workflows/sample.yml

on:
  workflow_dispatch: // To run manually
    inputs:
      stage:
        description: 'which environment'
        required: true
        default: 'production'
      tag:
        description: 'docker image tag name'
        required: false
        default: 'latest'

      ***

      ${{ github.event.inputs.stage }}
      ${{ github.event.inputs.stage }}

      ***
```

## When Run Manually
> If we run this workflow from a GitHub browser, we must enter values for the required inputs manually before the workflow will run.
 
We can use the entered values in yml file by `${{ github.event.inputs.stage }}` and `${{ github.event.inputs.stage }}`.

## Reference
- [GitHub Docs : Events that trigger workflows - workflow_dispatch](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#workflow_dispatch)
