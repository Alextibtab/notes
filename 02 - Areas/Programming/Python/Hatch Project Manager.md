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
You can use `hatch new --init` to initialise an already existing python project and hatch will automatically migrate any `setuptools` 