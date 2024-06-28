---
layout: post
title: "How to Change Display Brightness Using Xrandr"
subtitle: ""
background: ''
---

Find your display name or identifier.
```sh
xrandr --prop | grep " connected"
```

you will get an output like this:
```
eDP connected primary 1920x1080+0+0 (normal left inverted right x axis y axis) 344mm x 194mm
```
The first string here is the identifier (here its eDP).

To check current brightness value.
```sh
xrandr --prop --verbose | grep -A10 " connected" | grep "Brightness"
```

To change brightness (replace eDP with your identifier)
```sh
xrandr --output eDP --brightness 0.4
```
0.1 for the lowest and 1 for the maximum brightness.