# Python CLI Tools

- [Python CLI Tools](#python-cli-tools)
  - [Bandit](#bandit)


## Bandit

![SAST](https://img.shields.io/badge/Category-SAST-blue)

Quick facts

* Easy to integrate with **pre-commit**
* Easy to install with `pip install bandit`
* Easy to run:
  * On one file: `bandit $file_name`
  * Recursively: `bandit -r .`
* Configurable in pyproject.toml

[Bandit](https://github.com/PyCQA/bandit) is a project by
[PyCQA](https://github.com/PyCQA) that searches for common security issues in
Python code bases.
