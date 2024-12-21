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

The `__init__.py` is recommended as it lets user import the directory