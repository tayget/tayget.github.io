---
layout: post
title: "Enable simultaneous output in linux"
subtitle: "Multiple audio outputs at once"
background: ''
---

Install paprefs.

Ubuntu/Debian
```sh
sudo apt install paprefs
```

Arch
```sh
sudo pacman -S paprefs
```
OpenSUSE
```sh
sudo zypper install paprefs
```

Run paprefs
```sh
paprefs
```

Enable simultaneous output 

![paprefs_image](/img/posts/simultaneous-output/paprefs.png)

Now connect all the bluetooth devices to the system.

Open pavucontrol

If not installed:

Ubuntu/Debian
```sh
sudo apt install pavucontrol
```

Arch
```sh
sudo pacman -S pavucontrol
```
OpenSUSE
```sh
sudo zypper install pavucontrol
```


```sh
pavucontrol
```

Make sure simultaneous output is enabled.

![pavu-image](/img/posts/simultaneous-output/pavucontroller.png)

