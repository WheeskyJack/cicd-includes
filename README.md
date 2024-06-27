# cicd-includes
CI/CD includes to be used by other projects. This project is holding the common test, linter etc jobs. 

Currently, it supports golang test and lint.

## Usage
sample example on how to call this reusable workflow in your repository : 

you can add similar yml as shown below in your repository's .github/workflows directory.

```yml
name: golang lint and test

on:
  push:
    branches:
      - master
      - main
  pull_request:
    branches:
      - master
      - main

permissions:
  contents: read
  # Optional: allow read access to pull request. Use with `only-new-issues` option.
  # pull-requests: read

jobs:
  Lint-App:
    uses: WheeskyJack/cicd-includes/.github/workflows/golangci-lint.yml@v1.2.0
  Test-App:
    uses: WheeskyJack/cicd-includes/.github/workflows/go_test.yml@v1.2.0

```

## Contributing
Contributions are welcome! Please feel free to create an issue and submit a pull request.

## License

This project is licensed under the <a href="https://github.com/WheeskyJack/cicd-includes/blob/main/LICENSE">MIT License</a> - see the LICENSE file for details.
