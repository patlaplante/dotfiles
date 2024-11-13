---
creation date: 2024-11-04 13:45
modification date: Monday, 4th November 2024, 13:45:47
tags:
  - shell
---
---
## references

```cardlink
url: https://github.com/nushell/awesome-nu
title: "GitHub - nushell/awesome-nu: A curated list of awesome tools that work within the nu language ecosystem e.g. nushell, scripts, nana, etc."
description: "A curated list of awesome tools that work within the nu language ecosystem e.g. nushell, scripts, nana, etc. - nushell/awesome-nu"
host: github.com
favicon: https://github.githubassets.com/favicons/favicon.svg
image: https://opengraph.githubassets.com/858183f70c71b65f8a62d2ac523575148945309eca6edf5cd0764c1b1dc12921/nushell/awesome-nu
```

---
## using vim by default

```
# At the bottom $nu.env-path 
# Will allow you to use config env or config nu
$env.EDITOR = "nvim"
```

```
# Choose vi for vi cli mode in $nu.config-path
edit_mode: vi
```

## running system command like open

### [Escaping to the System](https://www.nushell.sh/book/escaping.html#escaping-to-the-system)

Nu provides a set of commands that you can use across different OSes ("internal" commands), and having this consistency is helpful. Sometimes, though, you want to run an external command that has the same name as an internal Nu command. To run the external [`ls`](https://www.nushell.sh/commands/docs/ls.html) or [`date`](https://www.nushell.sh/commands/docs/date.html) command, for example, you use the caret (^) command. Escaping with the caret prefix calls the command that's in the user's PATH (e.g. `/bin/ls` instead of Nu's internal [`ls`](https://www.nushell.sh/commands/docs/ls.html) command).

Nu internal command:

```
> ls
```

Escape to external command:

```
> ^ls
```

Open the finder window:

```
> ^open .

#or define an alias
> : alias open = ^open
> open .
```

### [Windows Note](https://www.nushell.sh/book/escaping.html#windows-note)

When running an external command on Windows, nushell [used to](https://www.nushell.sh/blog/2022-08-16-nushell-0_67.html#windows-cmd-exe-changes-rgwood) use [Cmd.exe](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/cmd) to run the command, as a number of common commands on Windows are actually shell builtins and not available as separate executables. [Coming from CMD.EXE](https://www.nushell.sh/book/coming_from_cmd.html) contains a list of these commands and how to map them to nushell native concepts.