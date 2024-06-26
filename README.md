# Terminus Install Action

[![Test](https://github.com/pantheon-systems/action-terminus-install/actions/workflows/test.yml/badge.svg)](https://github.com/pantheon-systems/action-terminus-install/actions/workflows/test.yml)
[![MIT License](https://img.shields.io/github/license/pantheon-systems/action-terminus-install)](https://github.com/pantheon-systems/action-terminus-install/blob/main/LICENSE)

Installs Terminus for use in GitHub Actions.

## Inputs

### `os`

The operating system to install Terminus on. Default `"ubuntu-latest"`. Currently accepts `"ubuntu-latest"` and `"macos-latest"`.

## Usage

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    - uses: shivammathur/setup-php@v2
      with:
        php-version: 8.3
    - uses: jazzsequence/action-terminus-install@v1
      with:
        os: ubuntu-latest
    - run: terminus --version
```

## Notes

* Adding a step to install PHP is not required _except when using macos-latest_ as the operating system. Since Terminus is a PHP application, it requires PHP to be installed on the system. The `shivammathur/setup-php` action is used in the example above to install PHP. If you are using a different action to install PHP, you can skip this step.
