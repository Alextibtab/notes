---
Area: Programming
Language: Python
tags:
  - programming
  - python
---
# Packaging Python projects

[Python Packaging Example](https://packaging.python.org/en/latest/tutorials/packaging-projects/)

The official packaging guide recommends to create a src folder for storing packages in.
```
directory/
└── src/
    └── example_package/
        ├── __init__.py
        └── example.py
```

The `__init__.py` is recommended as it lets user import the directory as a package.

Then `example.py` is an example of a module within the package that could contain the logic of the package.

### Package Template

```
packaging_tutorial/
├── LICENSE
├── pyproject.toml
├── README.md
├── src/
│   └── example_package/
│       ├── __init__.py
│       └── example.py
└── tests/
```

a typical python package will have the above file structure.