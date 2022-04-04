# Test Workshop

## Sette opp virtualenv, flake8 og pytest.
1. `virtualenv .venv` - Workshop om virtualenvironment handling noen?
2. `pip install flake8`
3. `pip install pytest`

## TODO
Dette er jo en workshop, i mangel på kreativitet skal vi lage en romer-tall-converter.
1. Lag en mappe som heter `tests`
2. Lag en enkel test `test_roman_converter.py`
3. Kjør med pytest/eventuelt sett opp VSCODE

## Sette opp pre-commit
1. Installer `pip install pre-commit`
2. Sjekk at funker `pre-commit --version`
3. Lag en `.pre-commit-config.yaml`
```yaml
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.3.0
    hooks:
    -   id: check-yaml
    -   id: end-of-file-fixer
    -   id: trailing-whitespace
-   repo: https://github.com/pycqa/flake8
    rev: 
    hooks:
    -   id: flake8
```
5. Installer scriptet `pre-commit install`
6. Cheat-sheet:
    * `pre-commit` run: this is what pre-commit runs by default when committing. This will run all hooks against currently staged files.
    * `pre-commit run --all-files/-a`: run all the hooks against all the files. This is a useful invocation if you are using pre-commit in CI.
    * `pre-commit run flake8`: run the flake8 hook against all staged files.
    * `git ls-files -- '*.py' | xargs pre-commit run --files`: run all hooks against all *.py files in the repository.

