# Python CLI Tools

- [Python CLI Tools](#python-cli-tools)
  - [Bandit](#bandit)


## Bandit

![SAST](https://img.shields.io/badge/Category-SAST-blue)

[Bandit](https://github.com/PyCQA/bandit) is a project by
[PyCQA](https://github.com/PyCQA) that searches for common security issues in
Python code bases.

* Install:
  * `pip install bandit`
  * pre-commit - See **cli_tools/pre-commit/python.pre-commit-config.yaml**
* Configure:
  * `pyproject.toml`
* Run:
  * via pre-commit.
  * `bandit $file_name` to run on a single file.
  * `bandit -r .` to run recursively.
