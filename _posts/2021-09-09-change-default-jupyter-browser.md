---
layout: post
title: "How do I change the default browser used by the Jupyter notebook?"
subtitle: ""
background: ''
---

Create a Jupyter Notebook Config file.

```sh
jupyter notebook --generate-config
```

Then you go to

```sh
~/.jupyter/jupyter_notebook_config.py
```

Find you browser path, in my case Chromium

```sh
which chromium
```

Find this line ```#c.NotebookApp.browser = ''``` in the config file and change it to ```c.NotebookApp.browser = 'your browser path'```

In my case 
```
c.NotebookApp.browser = '/usr/bin/chromium'
```