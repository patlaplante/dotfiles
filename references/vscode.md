---
creation date: 2024-11-04 13:30
tags:
  - computer/ide
  - computer/software
---

## file nesting

This enables hiding header files under source file.
![[Screenshot 2024-11-07 at 10.01.11.png]]

```
  "explorer.fileNesting.enabled": true,
  "explorer.fileNesting.patterns": {
    "*.cts": "${capture}.typegen.ts",
    "*.js": "${capture}.js.map, ${capture}.min.js, ${capture}.d.ts",
    "*.jsx": "${capture}.js",
    "*.mts": "${capture}.typegen.ts",
    "*.ts": "${capture}.js, ${capture}.typegen.ts",
    "*.tsx": "${capture}.ts, ${capture}.typegen.ts",
    "*.c": "${capture}.h",
    "*.cpp": "${capture}.h",
    "package.json": "package-lock.json, yarn.lock, pnpm-lock.yaml",
    "tsconfig.json": "tsconfig.*.json"
  },
```


## issues
### starship fonts not showing correctly in integrated terminal

```
mkdir -p ~/.local/share/fonts
ln -s ~/.local/share/fonts/
~/.fonts 
cd ~/.fonts 
curl -OL https://github.com/ryanoasis/nerd-fonts/releases/latest/download/Hack.tar.xz 
tar -xvf Hack.tar.xz
```

Add to settings `"terminal.integrated.fontFamily": "Hack Nerd Font",`

---
### references

```cardlink
url: https://www.youtube.com/watch?v=9_I0bySQoCs
title: "Transforming VS Code: Beyond Themes! — Make VS Code Unrecognizable!"
description: "In this video, we will explore how to customize VS Code beyond the usual options available through themes. We will significantly alter various aspects of the..."
host: www.youtube.com
favicon: https://www.youtube.com/s/desktop/97e0e051/img/logos/favicon_32x32.png
image: https://i.ytimg.com/vi/9_I0bySQoCs/maxresdefault.jpg
```

