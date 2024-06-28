---
layout: post
title: "How To Switch Between Nvidia and Non-Nvidia Graphics Card on Ubuntu"
subtitle: ""
background: ''
---

Install recommended driver for your device:
```sh
sudo ubuntu-drivers devices
```

In my case it is ```nvidia-driver-470```:
```sh
sudo apt install nvidia-driver-470
```

Also install Nvidia Settings & Nvidia Prime:
```
sudo apt install nvidia-settings nvidia-prime
```

Reboot.

To switch between Nvidia and Non-Nvidia Cards:

Note: AMD users also chooses intel.

```sh
nvidia-settings
```
Go to Active Profile and choose intel(Power Saving Mode) ```# also for amd users``` for iGPU and Nvidia(Performance Mode) for Dedicated GPU.

OR

You can set which card to use as default:
```sh 
sudo prime-select intel <or nvidia>
```

You can also switch cards using:
```sh
sudo prime-switch intel <or nvidia>
```