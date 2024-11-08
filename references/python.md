---
creation date: 2024-11-04 13:52
modification date: Monday, 4th November 2024, 13:52:12
tags:
  - computer/coding/language
---

Before installing python using asdf, install the following dependencies

```shell
brew install ncurses
brew install readline

```

```shell
asdf plugin-add python

```

## nushell
To use venv
```sh
# source is not a valid command in nushell
overlay use .venv/bin/activate.nu
```