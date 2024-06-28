---
layout: post
title: "Export and Import Custom Shortcuts in Linux Mint"
subtitle: ""
background: ''
---


Make sure ```dconf-cli``` package is installed

To export your keyboard shortcuts to a file:
```sh
dconf dump /org/cinnamon/desktop/keybindings/ > dconf-settings.conf
```

To import the file after making any desired keybinding changes:
```sh
dconf load /org/cinnamon/desktop/keybindings/ < dconf-settings.conf
```