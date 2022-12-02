# copier-template-python

This is my [copier](https://github.com/copier-org/copier/) template for Python projects. 


## Features

- simple README.md
- pyproject.toml
- src layout
- `__about__.py`, `__init__.py`, and `__main__.py` files
- tests directory
- dual licence (Apache 2.0 + MIT)


## Requirements

```bash
pipx install copier
```


## Usage

### New Project
```bash
copier copy gh:patrickarmengol/copier-template-python <path/to/project>
```

### Updating

```bash
copier update <path/to/project>
```

### Post-copy Actions

Copier tasks are executed every update ATM. Issue [#240](https://github.com/copier-org/copier/issues/240) is tracking improvements to the tasks system, so hopefully soon we can specify pre/post+copy/update. I did find temporary solution using a hooks script within the project directory that is executed and deleted post copy/update, but it is not ideal. So, for now, I'll write some steps here for reference.

```
python -m venv venv
source venv/bin/activate
git init
git add .
git commit -m "initial commit"
```