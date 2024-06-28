---
layout: post
title: "How to Setup Touchpad Gestures in Ubuntu"
subtitle: ""
background: ''
---

Install Fusuma

Set your user to be a memeber of the input group, so than fusuma can read touchpad inputs.

```sh
sudo gpasswd -a $USER input
```

Then, you shall install libinput-tools and xdotool.
```sh
sudo apt-get install libinput-tools
```
```sh
sudo apt-get install xdotool
```

Now Install Ruby for Gem Package Manager.
```sh
sudo apt install ruby
```

Install Fusuma.
```sh
gem install fusuma
```

Configure the gestures.

Create a folder for fusuma in $HOME/.config/
```sh
mkdir $HOME/.config/fusuma
```

Now create a ```config.yml``` file in this folder.

```sh
touch $HOME/.config/fusuma/config.yml
```

Paste this config in ```config.yml```

```yml
swipe:
  3: 
    left: 
      command: 'xdotool key alt+Right'
    right: 
      command: 'xdotool key alt+Left'
    up: 
      command: 'xdotool key super'
    down: 
      command: 'xdotool key super'
  4:
    left: 
      command: 'xdotool key ctrl+alt+Down'
    right: 
      command: 'xdotool key ctrl+alt+Up'
    up: 
      command: 'xdotool key ctrl+alt+Down'
    down: 
      command: 'xdotool key ctrl+alt+Up'
pinch:
  in:
    command: 'xdotool key ctrl+plus'
  out:
     command: 'xdotool key ctrl+minus'

threshold:
  swipe: 0.4
  pinch: 0.4

interval:
  swipe: 0.8
  pinch: 0.1

```

Now you can assign custom shortcuts and make the appropriate changes in the ```config.yml``` file.

To start fusuma, run:
```sh
fusuma
```

Incase you get an error, try:
```sh
sudo fusuma 
```

Set this command as startup application.

