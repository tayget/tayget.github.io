---
layout: post
title: "How to connect bluetooth in arch"
subtitle: ""
background: ''
---

Install neccesary packages.

```sh
sudo pacman -S bluez bluez-utils blueman pulseaudio-bluetooth
```
```blueman``` - bluetooth manager.

```pulseaudio-bluetooth``` - bluetooth extension for pulseaudio.

```bluez bluez-utils``` - bluetoothctl.

Start bluetooth service.
```sh
sudo systemctl enable bluetooth.service
```

Reboot.

Now Connect to Bluetooth device using bluetooth manager