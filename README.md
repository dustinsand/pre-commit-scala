[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/dustinsand/pre-commit-scala)

pre-commit-scala
===============

A collection of git hooks for Scala to be used with the [pre-commit framework](http://pre-commit.com).

## Requirements

pre-commit-scala requires the following to run:

  * [pre-commit(2.8+)](http://pre-commit.com)
  * [Coursier](https://get-coursier.io/)

## Install

1. create `.pre-commit-config.yaml` in your git project
2. pre-commit install

example `.pre-commit-config.yaml`:

```yaml
- repo: https://github.com/dustinsand/pre-commit-scala
  rev: vX.X.X
  hooks:
    - id: scalafmt
      args: [--config, my-scalafmt.conf]
```

## Available Hooks

| Hook name       | Description                                                                                        |
| --------------- | -------------------------------------------------------------------------------------------------- |
| `scalafmt`           | Runs [Scalafmt](https://scalameta.org/scalafmt/) code formatter on Scala source files. |

### Notes about the `scalafmt` hook

To specify a custom scalafmt configuration, simply pass the argument to the hook:

```yaml
    - id: scalafmt
      args: [--config, my-scalafmt.conf]
```
