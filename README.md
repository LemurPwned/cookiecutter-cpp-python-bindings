# Cookiecutter template for a C++ with Python bindings

Creates a python package that can mix C++ bindings and pure Python code.

## Structure:

The structure is adjustable. Main parts are bindings, found `python` folder and pure Python code is to be placed in `python` folder. If you want to rename, adjust `setup.py` accordingly.
```
- repo_name/
    - README.md
    - setup.py
    - pyproject.toml
    - CMakeLists.txt
    - .gitignore
    - .pre-commit-config.yaml
    - python                        # C++ source file
        - module.cpp 
    - repo_name/
        - __init__.pyi              # Python interface file for C++ bindings
        - py.typed
        - src/                      # Pure Python part of the package
            - __init__.py 
            - repo_name.py
```
## Requirements:

- [Pybind11](https://pypi.org/project/pybind11/)
- [CMake](https://cmake.org)

## Installation

To set up install install Pybind11:
```
$ python3 -m pip install pybind11[global]
```
and then run the following command:

```bash
$ cookiecutter https://github.com/LemurPwned/cookiecutter-cpp-python-bindings.git
```
