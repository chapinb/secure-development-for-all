# Python CLI Tools

- [Python CLI Tools](#python-cli-tools)
  - [Bandit](#bandit)
  - [mypy](#mypy)


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


## mypy

![Type Checker](https://img.shields.io/badge/Category-Type%20Checker-green)

[mypy](https://github.com/python/mypy) is a project by the Python Software Foundation
that provides static type checking using Python's type hints.

* Install:
  * `pip install mypy`
  * pre-commit - See **cli_tools/pre-commit/python.pre-commit-config.yaml**
    * Note: You may neeed to configure `additional_dependencies` to import stubs. [See the docs here](https://github.com/pre-commit/mirrors-mypy).
* Configure:
  * `pyproject.toml` and other methods [described in their documentation](https://mypy.readthedocs.io/en/stable/config_file.html)
* Run:
  * via pre-commit
  * `mypy .`
  * `mypy some_module/some_file.py`
