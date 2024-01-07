# python-template

Template repository for python repos.

## Setup

Create a virtual environment:
```bash
py -3.12 -m venv .venv
```

Activate the virtual environment:
```bash
.venv\Scripts\activate
```

Install the dependencies:
```bash
pip install .[dev]
```
> [!NOTE]
> You can also install just the build dependencies with `pip install .`

> [!NOTE]
> And instead of `pip install [some-package]`, you should rather add it to pyproject.toml

## Rationale

This is a template repository for python repos. It is intended to be used as a starting point for new python projects, and to provide a consistent structure. It includes the following:

- A `README.md` file with a basic description of the project.
- A `LICENSE` file with the MIT license.
- A `pyproject.toml` file with the following:
  - A `project` section with the project name, version, description, author, dependencies, and dev dependencies.
  - A `tool.ruff` section for specifying linting and formatting rules using Ruff, with strict yet sensible defaults.
  - A `tool.mypy` section for specifying type checking rules using mypy.
- A `.vscode` folder with the following:
  - A `settings.json` with sensible defaults for VS Code.
  - A `extensions.json` with the recommended extensions for VS Code python projects.

### Ruff

Ruff is a linter and formatter for python, written in Rust. I've used every single linter and formatter combination out there, and it's just the best, hands down. Everything else is either slow, doesn't work well together, doesn't give all the options I want, or doesn't work well with VSCode. Just use Ruff.

### MyPy

How I with Ruff had mypy support already, but alas, it does not. So we need Mypy. Mypy is a type checker if you don't know. I've set it to be very strict, but you can change that in the `pyproject.toml` file.

### PyTest

Eh, just because I'm used to it.