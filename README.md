# Terminus Install Action

[![Test](https://github.com/pantheon-systems/action-terminus-install/actions/workflows/test.yml/badge.svg)](https://github.com/pantheon-systems/action-terminus-install/actions/workflows/test.yml)
[![Actively Maintained](https://img.shields.io/badge/Pantheon-Actively%20Maintained-yellow?logo=pantheon&color=FFDC28)](https://docs.pantheon.io/oss-support-levels#actively-maintained-support)
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
	- uses: pantheon-systems/action-terminus-install@v1
	  with:
		os: ubuntu-latest
	- run: terminus --version
```
