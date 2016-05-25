---
layout: post
section-type: post
title: make your vim support lua
category: tech
tages: ['skills']
---

Vim is editors' god while emacs is god's editor.The default version of vim installed on mint is 7.4 with no support of lua, since we may need some special features that depend on lua, it must be done to make our vims lua-support.

## check vim version
To check your vim version, type in terminal:

```bash
 vim --version | grep lua
```

if it occurs to be like

```bash
 -lua
```
your vim is not lua-support.

## install vim-nox
the most convenient way is installing vim-nox

```bash
sudo apt-get install vim-nox
```
now we check the vim version again, it will be like

```bash
+lua
```
