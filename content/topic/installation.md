---
title: "Installation"
date: 2018-06-25T18:50:09+02:00
draft: true
weight: 1000
---

Sublime Six is implemented as a Python plugin
without any external dependencies.

The easiest way to install Six
is through [Package Control](https://packagecontrol.io/),
a package manager for Sublime Text.

To install Six,
look for the [Six](https://packagecontrol.io/packages/Six) package in Package Control
and install it.

After installing Six,
restart Sublime Text.
Six should then load
and enter normal mode.

### Channels

Six is available through two channels:
stable and dev.

After installing Six,
you are automatically subscribed to the stable channel.

Stable builds are published less often than dev builds,
but in exchange they tend to be more stable.

All builds are regularly tested
on Linux, macOS and Windows.

If you want to use the dev channel,
you need to open your Package Control settings
(located in *Packages/User*)
and add the following line:

    "install_prereleases": ["Six"]


### Uninstallation

If you want to uninstall Six,
use the corresponding Package Control command
or delete *Packages/Six*.
