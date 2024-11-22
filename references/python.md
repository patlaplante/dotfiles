---
creation date: 2024-11-04 13:52
modification date: Monday, 4th November 2024, 13:52:12
tags:
  - dev/language/python
---

Before installing python using asdf, install the following dependencies

```shell
# os/macos
brew install ncurses
brew install readline

# os/linux 
sudo apt install libncurses-dev libreadline-dev libssl-dev libbz2-dev libsqlite3-dev lzma python3-tk

sudo apt-get install libffi-dev
sudo apt-get install lzma
sudo apt-get install liblzma-dev
sudo apt-get install libbz2-dev
sudo apt install tk-dev
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