---
title: "Disabling Six for Selected Views"
date: 2018-06-27T07:42:21+02:00
draft: true
weight: 2000
---

Some Sublime Text plug-ins
may not interact well with Six.
This is specially true
for plug-ins that use *command mode*
to implement Vim-style navigation with regular keys
(for example, k and j to move up and down).
In such cases, it's possible to selectively disable Six for some views.

To disable Six for a given view,
set any of the following view settings to `true`:

- `__vi_external_disable`
- `__vi_external_disable_keys`

Both settings currently have the same effect:
Six will not be available in the corresponding view
(key presses will not be intercepted).

This configuration should normally be made
by the affected plug-in.
