---
creation date: 2024-11-04 22:14
modification date: Monday, 4th November 2024, 22:14:05
tags:
  - computer/shell/prompt
---
```cardlink
url: https://starship.rs
title: "Starship: Cross-Shell Prompt"
description: "Starship is the minimal, blazing fast, and extremely customizable prompt for any shell! Shows the information you need, while staying sleek and minimal. Quick installation available for Bash, Fish, ZSH, Ion, Tcsh, Elvish, Nu, Xonsh, Cmd, and Powershell."
host: starship.rs
favicon: https://starship.rs/icon.png
image: https://starship.rs/icon.png
```

```zsh
brew install starship
```

## Zsh 

Add the following to the end of `~/.zshrc`:

```sh
# ~/.zshrc

eval "$(starship init zsh)"
```

## Nushell 

WARNING
This will change in the future. Only Nushell v0.78+ is supported.

Add the following to the end of your Nushell env file (find it by running `$nu.env-path` in Nushell):

```sh
mkdir ~/.cache/starship
starship init nu | save -f ~/.cache/starship/init.nu
```

And add the following to the end of your Nushell configuration (find it by running `$nu.config-path`):

```sh
use ~/.cache/starship/init.nu
```
