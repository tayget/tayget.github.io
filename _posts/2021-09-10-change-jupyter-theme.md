---
layout: post
title: "Install Custom Theme in Jupyter Notebook"
subtitle: ""
background: ''
---

Install Jupyter Themes using pip

```sh 
pip install jupyterthemes
```
Change theme with:

```sh
jt -t <theme-name>
```

Available themes:

- onedork
- grade3
- oceans16
- chesterish
- monokai
- solarizedl
- solarizedd

My Config for Jupyter Notebook:

```sh 
jt -t gruvboxd -f inputmono -fs 13 -ofs 11 -cellw 88% -T
```