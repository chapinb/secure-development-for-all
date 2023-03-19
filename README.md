# Secure Development for All

A collection of resources to make it easy to add secure development practices
to your project.

![License](https://img.shields.io/github/license/chapinb/secure-development-for-all)

Table of Contents

- [Secure Development for All](#secure-development-for-all)
- [Goals](#goals)
- [Tools](#tools)
  - [IDE Extensions](#ide-extensions)
    - [Visual Studio Code](#visual-studio-code)
    - [PyCharm](#pycharm)
    - [Vim](#vim)
  - [CLI tools](#cli-tools)
    - [pre-commit](#pre-commit)
    - [gitleaks](#gitleaks)
    - [Semgrep](#semgrep)
  - [Continuous Integration tools](#continuous-integration-tools)
    - [GitHub Actions](#github-actions)
    - [GitLab CI](#gitlab-ci)
    - [Jenkins](#jenkins)

The [Tools](#tools) section has a number of options that can be used in
concert or independent with eachother. They are ordered in the ease of
implementation, from easiest to most difficult. Simultaneously they are
ordered from individual to team impact (as implementing it yourself is
naturally easier to do.)

# Goals

This is intended to help you get started or further mature your security
practices regarding security. Whether you are a full time developer, hobbiest,
or a scripter, there is something here to help you improve visibility into
the security posture of your projects.

Consider the following roadmap for implementation:

1. Install the [IDE extensions](#ide-extensions) into your editor and read
   about any findings the tools have, addressing them as appropriate.

2. Download some of the mentioned [CLI tools](#cli-tools) and run them against
   the whole project to see about any areas of improvement outside of your
   current working files.

3. Once you feel that your project meets the standards you would like, employ
   [Continuous Integration tools](#continuous-integration-tools) to enforce
   these standards on your code and future contributions. This increases
   consistency and confidence as your project evolves.

# Tools

Please consider opening a PR with your reccomendations about tools to add.

## IDE Extensions

[Back to Top](#secure-development-for-all)

The easiest place to start is by adding tools to your IDE that help identify
areas for improvement in your code. Some of these tools are similar across
editors while others are only available for a specific tool.

These sections and tools have no particular order.

### Visual Studio Code

* [SonarLint](https://www.sonarsource.com/products/sonarlint/)
* [Sourcery](https://sourcery.ai/)

### PyCharm

* [SonarLint](https://www.sonarsource.com/products/sonarlint/)
* [Sourcery](https://sourcery.ai/)

### Vim

* [ale](https://github.com/dense-analysis/ale)

## CLI tools

[Back to Top](#secure-development-for-all)

For language specific tools, please see the
[cli_tools/README.md](cli_tools/README.md).

### pre-commit

[pre-commit](https://pre-commit.com/) is a flexible tool that installs itself
as a git hook that can run a series of tools against only the changed files
in your project. Further, it can be installed to run before each commit,
enforcing checks on the files staged for commit.

* Install:
  * `pip install pre-commit`
* Configure:
  * `.pre-commit-config.yaml`.
  * Please see [cli_tools/pre-commit/README.md](cli_tools/pre-commit/README.md)
    for sample configuration files that you can employ in your project.
  * `pre-commit install --install-hooks` to install git hooks
* Run:
  * `git commit` to run against staged changes once the git hook is installed
  * `pre-commit run` to run against staged changes
  * `pre-commit run --all` to run against all files

As an additional level, you can have your continuous integration (CI) service
execute these same tasks across your merge request changes or entire code base
to validate the compliance with the pre-commit configuration.

### gitleaks

[Gitleaks](https://github.com/gitleaks/gitleaks) will scan your commit history
and staged changes for signs of possible secrets.

* Install:
  * `brew install gitleaks`
  * `docker pull ghcr.io/zricethezav/gitleaks:latest`
  * clone and `make build`
* Configure:
  * `.gitleaks.toml`
* Run:
  * Supports pre-commit
  * `gitleaks detect` will scan git history
  * `gitleaks protect` will scan your staged changes

### Semgrep

[Semgrep](https://github.com/returntocorp/semgrep) is a static application
security testing tool that provides support for multiple languages.

* Install:
  * `brew install semgrep`
  * `pip install semgrep`
  * `docker pull returntocorp/semgrep`
* Configure:
  * YAML - See https://semgrep.dev/docs/
* Run:
  * `semgrep scan --config auto` will scan with default settings

## Continuous Integration tools

[Back to Top](#secure-development-for-all)

### GitHub Actions

### GitLab CI

### Jenkins
