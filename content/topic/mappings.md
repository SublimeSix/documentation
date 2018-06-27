---
title: "Mappings"
date: 2018-06-27T07:08:13+02:00
draft: true
---

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

You can use a *User/sixrc.py* file to persist mappings.

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
