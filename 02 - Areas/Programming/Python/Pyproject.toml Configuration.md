---
Area: Programming
Language: Python
tags:
  - programming
  - python
  - cicd
  - automation
cssclasses:
---
# PyProject.toml
`pyproject.toml` is a configuration file used by many tools such as linters, type checkers...

### Useful TOML tables
- `[build-system]` lets you specify what build backend to use and what dependencies are needed
- `[project]` build system will use this table to obtain metadata about the project such as dependencies, author, tags etc...
- `[tool]` used to configure specific tools, e.g. `[tool.black]`, `[tool.mypy]` 

### Declaring the build backend
The `[build-system]` table contains a `build-backend` key which specifies what build backend to use. The `requires` key is a list of dependencies this backend requires to build the project normally just the backend package itself.

#### examples
```toml
[build-system]
    requires = ["hatchling"]
    build-backend = "hatchling.build"
```

### Static vs Dynamic metadata
Most of the time you will just write the value of a field e.g. `requires-python = ">= 3.8"`
