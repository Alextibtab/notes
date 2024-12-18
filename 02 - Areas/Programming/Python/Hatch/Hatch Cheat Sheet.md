---
Area: Programming
Language: Python
tags:
  - programming
  - python
  - cicd
  - cheatsheet
  - automation
cssclasses:
---
# Hatch Cheat Sheet
## Useful Commands
`hatch run`

## Example pyproject.toml
```toml
[build-systeml]
requires = ["hatchling"]
build-backend = "hatchling.build"

[project]
name = "basic-project"
requires-python = ">= 3.9"
authors = [
    {name = "foo", email = "foo@bar.com"}    
]
maintainers = [
    {name = "foo", email = "foo@bar.com"}    
]
description = "Example"
readme = "README.md"
keywords = ["Python Project", "Cheatsheet"]
classifiers = [
    "Development Status :: 3 - Alpha"
]
dependencies = [
    "numpy"
    "pandas"
]
dynamic = ["version"]

[project.optional-dependencies]
dev = ["tox", "ruff", "invoke"]

[project.urls]
Repository = "https://github.com/foo/sample.git"

[project.scripts]
example = "project:__main__.main_cli"

[project.gui-scripts]
example-gui = "project:__main__.main_gui"

[tool.hatch.version]
path = "src/project/__about__.py"

[tool.hatch.build.targets.wheel]
packages = ["src/project"]

[tool.hatch.envs.foo]
dependencies = [
    "cowsay"
]
features = [
    "dev"
]

[tool.hatch.envs.foo.scripts]
hello_world = "cowsay -t 'Hello, World!'"

[[tool.hatch.envs.test.matrix]]
python = ["3.11","4."]
```