# Secure Development for Everyone

A collection of resources to make it easy to add secure development practices
to your project.

Table of Contents

- [Secure Development for Everyone](#secure-development-for-everyone)
  - [Tools](#tools)
    - [IDE Extensions](#ide-extensions)
      - [Visual Studio Code](#visual-studio-code)
      - [PyCharm](#pycharm)
      - [Vim](#vim)
    - [CLI tools](#cli-tools)
      - [pre-commit](#pre-commit)
    - [Continuous Integration tools](#continuous-integration-tools)
      - [GitHub Actions](#github-actions)
      - [GitLab CI](#gitlab-ci)
      - [Jenkins](#jenkins)

The [Tools](#tools) section has a number of options that can be used in
concert or independent with eachother. They are ordered in the ease of
implementation, from easiest to most difficult. Simultaneously they are
ordered from individual to team impact (as implementing it yourself is
naturally easier to do.)

## Tools

Please consider opening a PR with your reccomendations about tools to add.

### IDE Extensions

The easiest place to start is by adding tools to your IDE that help identify
areas for improvement in your code. Some of these tools are similar across
editors while others are only available for a specific tool.

These sections and tools have no particular order.

#### Visual Studio Code

* [SonarLint](https://www.sonarsource.com/products/sonarlint/)
* [Sourcery](https://sourcery.ai/)

#### PyCharm

* [SonarLint](https://www.sonarsource.com/products/sonarlint/)
* [Sourcery](https://sourcery.ai/)

#### Vim

* [ale](https://github.com/dense-analysis/ale)

### CLI tools

#### pre-commit

[pre-commit](https://pre-commit.com/) is a flexible tool that installs itself
as a git hook that can run a series of tools against only the changed files
in your project. Further, it can be installed to run before each commit,
enforcing checks on the files staged for commit.

As an additional level, you can have your continuous integration (CI) service
execute these same tasks across your merge request changes or entire code base
to validate the compliance with the pre-commit configuration.

### Continuous Integration tools

#### GitHub Actions

#### GitLab CI

#### Jenkins
