---
title: "Differences with Vim"
date: 2018-06-25T19:52:32+02:00
draft: true
weight: 3000
---

Six strives to be as close to Vim
as the Sublime Text API permits.

Generally speaking,
the [Vim documentation](http://vimdoc.sourceforge.net/) should apply
equally to Six and Vim
as far as operators and motions are concerned.
Motions and operators in Six aim to be
100% ports of Vim's.

Six does not currently implement every single Vim feature,
but is designed to eventually become a comprehensive port.

The current focus of Six is
normal mode, visual and visual line modes,
and a subset of command-line mode.

Additionally, Six implements modes and features
that let you take advantage of unique Sublime Text features,
like multiple selections,
while keeping in with Vim principles.

### Non-standard Commands

Non-standard commands generally exist
to enable better interoperability with key Sublime Text features.

List of Six commands that are not standard Vim commands:

| Command            | Context             | Description                            |
| :----------------- | :------------------ | :------------------------------------- |
| `ctrl+j`           | autocomplete list   | next item                              |
| `ctrl+k`           | autocompoete list   | previous item                          |
| `ctrl+q`           | normal mode         | open Go To Symbol                      |
| `ctrl+shift+q`     | normal mode         | open Go To Symbol in Project           |

### Non-standard Modes

Non-standard modes generally exist
to enable better interoperability with key Sublime Text features.

Six includes two non-standard modes
with which you can take advantage of Sublime Text's multiple selections.

#### Multiple Selection Mode

Using the Multiple Selection Mode,
you can add selections
based on the word under the caret.

Commands available in Multiple Selection Mode:

| Command                     | Action                                   |
| :-------------------------- | :--------------------------------------- |
| <kbd>gh</kbd>               | Enter Multiple Selection Mode            |
| <kbd>j</kbd>                | Add selection                            |
| <kbd>k</kbd>                | Remove selection                         |
| <kbd>l</kbd>                | Skip selection                           |
| <kbd>J</kbd>                | Add all selections                       |
| <kbd>i</kbd>                | Enter Insert Mode                        |
| <kbd>Esc</kbd>              | Enter Normal Mode                        |

You cannot operate on text while in Multile Selection Mode.
Before operating on text,
switch to insert mode or to normal mode.

#### Multiple Line Selection Mode

Using the Multiple Line Selection Mode,
you can add lines.

Commands available in Multiple Line Selection Mode:

| Command                     | Action                                   |
| :-------------------------- | :--------------------------------------- |
| <kbd>gH</kbd>               | Enter Multiple Line Selection Mode       |
| <kbd>j</kbd>                | Add selection down                       |
| <kbd>k</kbd>                | Add selection up                         |
| <kbd>i</kbd>                | Enter Insert Mode                        |
| <kbd>Esc</kbd>              | Enter Normal Mode                        |

You cannot operate on text while in Multile Line Selection Mode.
Before operating on text,
switch to insert mode or to normal mode.

### Regular Expressions

Six uses
the same regular expressions' engine and synxtax for searches as Sublime Text.

The Vim regexp language is currently not supported.
