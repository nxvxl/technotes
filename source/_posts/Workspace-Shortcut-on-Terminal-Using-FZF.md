---
title: Workspace Shortcut on Terminal Using FZF
date: 2022-02-22 10:51:00
tags:
  - Terminal
categories:
  - Tips
---

Create a script to list directories and pipe it into FZF `~/.local/bin/workspace.sh`

```sh
#!/usr/bin/env bash

DIR=`ls $1 | fzf`

if [ -n "$DIR" ]; then
	clear
	cd "$1/$DIR"
fi
```

map CTRL+space using `bindkey` in `~/.zshrc`
```
bindkey -s '^ ' '. ~/.local/bin/workspace.sh /path-to-your-directory-here/^M'
```
