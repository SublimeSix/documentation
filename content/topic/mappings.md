---
title: "Mappings"
date: 2018-06-27T07:08:13+02:00
draft: false
weight: 5000
---

Support for mappings is partially implemented.

### Normal Mode Mappings

Six currently supports
non-recursive Vim mappings in normal mode.

To set a new mapping:

```
:nmap Y y$
```

To see available mappings:

```
:nmap
```

You can use a *User/sixrc.py* file to persist mappings
See the **Settings and Configuration** section for more information.

### Insert Mode Mappings

Mappings in insert mode can be defined
in a *.sublime-keymap* file.

For example:

```
{"keys": ["j", "j"], "command": "six_press_key", "args": {"key": "<Esc>"}, "context": [{"key": "six_is_in_insert_mode"}, {"key": "six_is_accepting_input", "operand": false}]}
```

The `six_is_accepting_input` context is generally necessary
to avoid disrupting commands that expect input,
like `c<motion>`, `/<input>`, etc.

This is the complete list of contexts
that you can use in *.sublime-keymap* files:

| Context | Description  |
| :------ | :----------- |
| `six_is_in_command_mode` | `true` if Six is in normal or any visual mode |
| `six_is_in_insert_mode` | `true` if Six is in insert mode |
| `six_is_in_multiple_selection_mode` | `true` if Six is in multiple selection mode |
| `six_is_accepting_input` | `true` if Six is currently accepting command input |
| `six_enable_ctrl_keys` | `true` if the `enable_ctrl_keys` setting is `true` |


{{% block note %}}
The Sublime Text API offers limited support to capture and process keys in insert mode. Therefore, insert mode mappings must be defined in *.sublime-keymap* files.
{{% /block %}}