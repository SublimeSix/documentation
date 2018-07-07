---
title: "Settings and Configuration"
date: 2018-06-25T19:38:49+02:00
draft: true
weight: 4000
---

Currently, you can configure Six
using two methods: a Sublime Six settings file, and an initialization script.
Both methods can be used at the same time.

### Configuring Six with a Sublime Settings File

To configure Six,
select **Preferences: Six Settings** from Sublime Text's command palette.
Two files will open side by side.
You can check the meaning of individual settings
in the file on the left-hand side,
but do only edit settings in the file on the right-hand side.

{{% block note %}}
Only settings stored in the *User/Six.sublime-settings* file
get saved. Settings stored in *Six/Six.sublime-settings*
will be overwritten with every update to Six.
{{% /block %}}

### Configuring Six with an Initialization Script

You can create a *User/sixrc.py* file
to customize some aspects of Six.
Watch the [sample sixrc.py](https://github.com/SublimeSix/sample-sixrc) repository
to see detailed instructions
and to keep up to date
with all the customization options.

{{% block note %}}
Vim options are not supported at the moment.
Future versions of Six will implement `:set`
and similar commands for managing settings.
{{% /block %}}

