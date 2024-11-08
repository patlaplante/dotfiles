
## cli tool
[[carapace]] 
A multi-shell completion **[library](https://github.com/carapace-sh/carapace)** and **[binary](https://github.com/carapace-sh/carapace-bin)**.  Very powerful.

[[m-cli]]
Mac configuration/control swiss army knife

[[zoxide]]
Better CD navigation.  Remembers where you've bin, making it quicker to get back to where you've been in the past.

```dataview
LIST FROM "references"
```

```dataviewjs
// Render a simple table of book info sorted by rating.
const table = dv.markdownTable(["cli", "os", "command", "desc"], dv.pages("#computer/cli")
    .sort(b => b.file.link)
    .map(b => [b.file.link, b.os, b.command, b.desc]))

dv.paragraph(table);
```

## ide
[[vscode]]

## language/compilers/toolchains
[[python]]
[[esp-idf]] - espressif (ESP32) toolchain

## package managements
[[homebrew]]
Using it over nix-os.  Nix os is much more powerful but requires sudo access, which I do not have on my company macbook

## prompts
[[starship]]
Very fast prompt.  Comparable to power10k

## shell
[[nushell]]
A new type of shell.  Really nice, but is very different from zsh/bash.  Currently investigating to get a feel on how I could use it.

## software
[[obsidian]] -- knowledge management
## system configurations
[[mac-system-settings]]
[[m-cli]]


