# Canonical documentation style guide

This repository contains the documentation and the Vale rules for the documentation style guide.

The style guide itself is written in Markdown and contained in the `en` directory.

It is published online at: [docs.ubuntu.com/en/styleguide](https://docs.ubuntu.com/styleguide/en)

## The Vale rules

The Vale linter operates from a series of rules. These are defined in individual YAML files, grouped into 'Styles'.
This repository contains the Canonical set of rules, or the Canonical Style. 

### Adding to the rules

Anyone is welcome to submit a PR to add additional rules. However, no additions will be considered unless they are part of the Canonical Style Guide as found at the website above.

For information on how to create rules, see the Vale [documentation on Styles][Vale styles].

### Using the rules

The Vale rules are published here so that they can be used in any workflow anywhere. You can run Vale locally, as part of CI or in a GitHub workflow - all you need is Vale, a configuration file (which you can also copy from this repository) and the Canonical Styles. Two common scenarios are also catered for more directly here, as detailed below.

## The Canonical Style GitHub action

This repository also includes a file, `action.yml`, which is the basis of a GitHub action to automatically run Vale checks on incoming pull requests. 

### Using the GitHub action in a workflow

Your repository can make use of the action in a workflow. An example workflow is included in this repository and is demonstrated here. Note that the style guide action is merely part of a functioning workflow.

```yaml
on: [pull_request]

jobs:
  vale:
    name: Style checker
    runs-on: ubuntu-22.04
    defaults:
        run:
            shell: bash
            working-directory: .
    steps:
        - name: Checkout repo to runner
          uses: actions/checkout@v3
        - name: Install styles
          uses: canonical/praecepta@main
        - name: Run Vale tests
          uses: errata-ai/vale-action@reviewdog
          with:
            files: ./docs
            fail_on_error: true
```

In the example above, the workflow is organised as a single job. This is important as the actions rely on persistence through the run.
There are three job steps:
 - The github/checkout action: this fetches the code from the repo calling the workflow
 - The style guide action: this fetches the styles and, if not present, a default config for Vale. The example fetches from the main branch since rules are currently under active development.
 - The vale/reviewdog action: this runs Vale using reviewdog, to insert comments into a pull-request

 This workflow uses reviewdog to insert output into review comments on any changes. The advantage of this method is:
  - the actions only run on new material (i.e. stuff added in the current PR)
  - it is surfaced directly where it will be noticed

[Vale styles]: https://vale.sh/docs/topics/styles/
