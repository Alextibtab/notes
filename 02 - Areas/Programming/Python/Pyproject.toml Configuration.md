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

#### Example
```toml
[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"
```

### Static vs Dynamic metadata
Most of the time you will just write the value of a field e.g. `requires-python = ">= 3.8"` or `version = "1.0"` 

However you can let the build backend compute some of this metadata. For example many build backends can read the version from a `__version__` attribute in code or Git tag. In this case you would mark the field as dynamic
#### Example
```toml
[project]
dynamic = ["version"]
```

### Project Table Fields

#### `name`
The project name must consist of ASCII letters, digits `_`, `-` and `.` but must not start or end with an underscore, hyphen or period.

```toml
[project]
name = "foo-bar
```

#### `version`
Project version number can be static or dynamic

```toml
[project]
version = "2024.0.0"
```

```toml
[project]
dynamic = ["version"]
```

#### `dependencies`
Project dependencies can be listed these should be required and not optional dependencies
```toml
[project]
dependencies = [
    "httpx",
    "gidgethub[http]>4.0.0",
    "django>2.1; os_name != 'nt'",
    "django>2.0; os_name == 'nt'",
]
```

#### `optional-dependencies`
Optional dependencies can be split into multiple keys making it easier to define dependencies for certain features such as `dev` dependencies for testing and formatting or `gui` dependencies for installing a project with GUI support

```toml
[project.optional-dependencies]
gui = ["PyQt5"]
dev = ["black", "ruff", "tox"]
```

Each of these keys define a "packaging extra" that mean when you pip install your project you can specify what dependencies to install `pip install project-name[gui,dev]`

