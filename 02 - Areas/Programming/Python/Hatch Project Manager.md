---
Area: Programming
Language: Python
tags:
  - programming
  - python
  - automation
  - cicd
---
[Hatch](https://hatch.pypa.io/latest/) is a modern python project manager

It has many features such as; project generation, environment management, build system, static analysis, dynamic versioning, testing, and publishing.

### Project Generation
To create a new project using hatch you can run the following command 
```bash
hatch new "Hatch Demo"
```

This will result in the following basic file structure
```
hatch-demo
├── src
│   └── hatch_demo
│       ├── __about__.py
│       └── __init__.py
├── tests
│   └── __init__.py
├── LICENSE.txt
├── README.md
└── pyproject.toml
```

hatch automatically creates the basic project layout with the pyproject.toml, README and LICENSE files then also creates a tests directory and the name of your project as a python package inside the src directory.

#### Existing projects
You can use `hatch new --init` to initialise an already existing python project and hatch will automatically migrate the `setup.py` file for `setuptools`

Like any other python tool it is now common to configure it inside the `pyproject.toml` using the `[tool]` table so to configure hatch you'd use
```toml
[tool.hatch]
option = "..."
```

### Environments

hatch environments let you automate python virtualenvs. When running any commands hatch will default to using the `default` environment unless an alternative is explicitly chosen.

#### Creation
environments can be created using the `hatch env create` command. However this isn't necessary as hatch will automatically trigger the creation whenever you try to spawn a shell or run a command that requires an environment.

to enter an environment you can use the `hatch shell` command that will you drop you into environment with your project already installed.

#### Dependencies
environments will work with normal project dependencies but you can also create custom environments that have additional specific dependencies if you wanted to create different environments for building, testing etc...

```toml
[tool.hatch.envs.docs]
dependencies = [
    "mkdocs"
]

[tool.hatch.envs.docs.scripts]
build = "mkdocs build --clean --strict"
server = "mkdocs serve --dev-addr localhost:8000"
```

the above example shows configuring an additional `docs` environment which you can also add custom scripts

to run the custom scripts you would run `hatch run docs:serve` if you wanted to gain a shell into the `docs` environment you'd run `hatch -e docs shell`

#### M
#### Removal
You can use `hatch env remove` to remove individual environments or `hatch env prune` to delete an entire projects environments