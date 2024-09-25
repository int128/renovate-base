# renovate-base [![renovate-config](https://github.com/int128/renovate-base/actions/workflows/renovate-config.yaml/badge.svg)](https://github.com/int128/renovate-base/actions/workflows/renovate-config.yaml)

A Renovate config for me.

## Getting Started

### .github/renovate.json5

```json5
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>int128/renovate-base",
  ],
}
```

### .github/workflows/validate.yaml

```yaml
name: validate

on:
  pull_request:
    paths:
      - .github/workflows/validate.yaml
      - .github/renovate.*
  push:
    branches:
      - main

jobs:
  validate:
    uses: int128/renovate-base/.github/workflows/validate.yaml@main
```
