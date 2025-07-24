---
title: "Fixing the upower warning - WSL/ZSH/Spaceship prompt"
datePublished: Fri Dec 11 2020 00:00:00 GMT+0000 (Coordinated Universal Time)
cuid: cmdhmgzid000v02lb8c21dabl
slug: fixing-upower-warning-wsl-zsh-spaceship

---


# Fixing the upower warning - WSL/ZSH/Spaceship prompt
*December 11, 2020*

The blog post discusses a warning that appears when using the Spaceship prompt in Windows Subsystem for Linux (WSL) with ZSH:

> (upower:26251): UPower-WARNING **: 10:47:25.757: Cannot connect to upowerd: Could not connect: No such file or directory

The author provides a solution to disable the battery status feature in the Spaceship prompt:

```bash
# Turn off power status when using spaceship prompt
export SPACESHIP_BATTERY_SHOW=false
```

This can be added to the `~/.profile` file to prevent the upower warning from appearing.

## Key Takeaways

- The warning occurs because upowerd is not running in WSL
- Disabling the battery status feature resolves the issue
- The fix can be implemented by setting an environment variable