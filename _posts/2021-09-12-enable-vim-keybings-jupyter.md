---
layout: post
title: "Enable Vim Keybindings in Jupyter Notebook"
subtitle: ""
background: ''
---

Install NbExtensions using pip

```sh
pip install jupyter_contrib_nbextensions
```

```sh
jupyter contrib nbextension install --user
```

Create a directory for Extensions.

```sh
mkdir -p $(jupyter --data-dir)/nbextensions
```

```sh
cd $(jupyter --data-dir)/nbextensions
```

Clone the repo

```sh
git clone https://github.com/lambdalisue/jupyter-vim-binding vim_binding
```

Activate Extension.

```sh
jupyter nbextension enable vim_binding/vim_binding
```