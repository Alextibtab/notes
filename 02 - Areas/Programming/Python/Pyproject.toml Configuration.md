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
name = "foo-bar"
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

#### `requires-python`
Declare the minimum version of python that's supported.

```toml
[project]
requires-python = ">= 3.9"
```

### Creating scripts

#### `[projects.scripts]`
To install a command as part of the package you can use the `[project.scripts]` table.

```toml
[project.scripts]
foo-cli = "foo:main"
```

this would let you run `foo-cli` in a terminal and it will automatically run the `main()` function defined in `foo`

#### `[project.gui-scripts]`
The default `[project.scripts]` requires a terminal to work so if this command was launched through a GUI it would open a terminal to avoid this the `[project.gui-scripts]` table can be used instead. **This difference is only relevant on windows**

```toml
[project.gui-scripts]
foo-gui = "foo:main_gui"
```

### About Your project

#### `authors`
List of authors for the project including name and/or an email address
```toml
[project]
authors = [
    {name = "Foo Bar", email = "foo@bar.com"},
    ...
]
```

#### `maintainers`
List of maintainers for the project including name and/or email address
```toml
[project]
maintainers = [
    {name = "Foo Bar", email = "foo@bar.com"},
    ...
]
```

#### `description`
Short one-line description of the project will be shown as a headline on PyPi and search results
```toml
[project]
description = "My Amazing Project!"
```

#### `readme`
A longer description that will typically point to either a `README.md` or `README.rst` file.

```toml
[project]
readme = "README.md"
```

#### `license`
Project license either a file or name of License
```toml
[project]
license = {file = "LICENSE"}
```

```toml
[project]
license = {text = "MIT License"}
```
if using a common license you can omit this field and instead use one of the classifiers starting with `License ::`

#### `keywords`
Keywords that will help PyPi search suggest your package
```toml
[project]
keywords = ["alpaca", "bar", "cheese"]
```

#### `classifiers`

A list of PyPI Classifiers

```toml
[project]
classifiers = [
    # How mature is this project?
    # 3 - Alpha
    # 4 - Beta
    # 5 - Production
    "Development Status :: 4 - Beta",

    # Intended Audience
    "Intended Audience :: Developers",
    "Topic :: Software Development :: Build Tools",

    # License
    "License :: OSI Approved :: MIT License",

    # Supported Python versions
    "Programming Language :: Python :: 3",
    "Programming Language :: Python :: 3.9",
]
```

to prevent a package from being uploaded to PyPI use the special `Private :: Do Not Upload` classifier. PyPI will always reject any package containing a classifier that begins with `Private ::`

#### `urls`

A list of URLs associated with the project such as project homepage, documentation and repository.

```toml
[project.urls]
Homepage = "https://example.com"
Documentation = "https://readthedocs.org"
Repository = "https://github.com/me/foo.git"
Issues = "https://github.com/me/foo/issues"
```

Advised to use well known labels as PyPI might render certain labels differently.

