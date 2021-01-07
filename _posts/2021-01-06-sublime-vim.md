---
layout: post
title: "Sublime text is your vim editor"
excerpt: "Vintage mode for vim; Sublime text shortcuts"
modified: 2021-01-05
tags: [blog]
comments: false
---
Vintage mode in Sublime text provide the vim enviroment.

- [Enable vintage mode](#enable-vintage-mode)
- [Vim cheat sheet](#vim-cheat-sheet)
  * [Navigation](#navigation)
  * [Bookmark](#bookmark)
  * [Insert mode](#insert-mode)
  * [Selecting](#selecting)
  * [Undo/Redo](#undo-redo)
  * [Finding](#finding)
  * [Delete/Copy/Paste](#delete-copy-paste)
  * [Format](#format)
- [Sublime shortcuts](#sublime-shortcuts)
  * [General](#general)
  * [Split window](#split-window)

# Enable vintage mode
In Preferences>Setting>User, add the following codes  
```
{
	"color_scheme": "Packages/Color Scheme - Default/Monokai.sublime-color-scheme",
	"font_size": 10,
	"ignored_packages":
	[
	],
	"theme": "Default.sublime-theme",
	"vintage_ctrl_keys": true
}
```

Default *Ctrl* key bindings in Sublime
- Ctrl+[: Escape
- Ctrl+R: Redo
- Ctrl+Y: Scroll down one line
- Ctrl+E: Scroll up one line
- Ctrl+F: Page Down
- Ctrl+B: Page Up

For my own convinience, I coustomerized the escape key to be *jj* by adding the following codes in preferences>key bindings>usr  
```
Custom escape key, in key binding
{ "keys": ["j", "j"], "command": "exit_insert_mode",
    "context":
    [
        { "key": "setting.command_mode", "operand": false },
        { "key": "setting.is_widget", "operand": false }
    ]
}
```
# Vim cheat sheet
## Navigation
Key|Description
---|---
**h b B ^ 0** | h-previous character; b-pervious work; B-pervious work and skip punctuation; ^-first non-blank character; 0-begining of line;    
**l e w E W $** | l-next character; e-end of word; w-begining of next word; E-end of Word; W-begining of next WORD; $-end of line
**k <kbd>Ctrl</kbd>+u <kbd>Ctrl</kbd>+b gg** | k-up 1 line; <kbd>Ctrl</kbd>+u-up 1/2 page; <kbd>Ctrl</kbd>+b-up 1 page; gg-first line;
**j <kbd>Ctrl</kbd>+d <kbd>Ctrl</kbd>+f G** | j-down 1 line; <kbd>Ctrl</kbd>+d-down 1/2 page; <kbd>Ctrl</kbd>+f-down 1 page; G-last line;
**j <kbd>Ctrl</kbd>+d <kbd>Ctrl</kbd>+f G** | j-down 1 line; <kbd>Ctrl</kbd>+d-down 1/2 page; <kbd>Ctrl</kbd>+f-down 1 page; G-last line;
_n_**gg** | Goto line _n_
<kbd>Shift</kbd> + * | jump to next word matching cursor (case insensitive)
<kbd>Shift</kbd> + **#** | jump to previous word matching cursor
<kbd>Shift</kbd> + **H**| move to high (header) part of screen
<kbd>Shift</kbd> + **M** | move to middle of screen
**zz** | center screen on cursor
**zt** | allgn top of screen on cursor
**zb** | allgn top of center screen on cursor
<kbd>Shift</kbd> + **L** | move to lower part of screen
<kbd>Shift</kbd> + **}** | Go next paragraph empty space
<kbd>Shift</kbd> + **{** | Go previous paragraph empty space
<kbd>Shift</kbd> + **%**|Jump to open/close (), {}, or []

## Bookmark
**m** _[a-z0-9]_|(book)mark current cursor position with register (any key _[a-z0-9]_)
**'** _[a-z0-9]_ |Return to marked position _[a-z0-9]_ (first non-blank character in line)
<kbd>Ctrl</kbd> + + **g**|Find All instances
**`** _[a-z0-9]_ | jump to line *and* column of mark
<kbd>Ctrl</kbd>+<kbd>F2</kbd> | Toggle Bookmark (with indicator)
<kbd>F2</kbd> | Jump to Next bookmark
<kbd>Shift</kbd>+<kbd>F2</kbd> | Jump to Previous bookmark
<kbd>Shift</kbd>+<kbd>Ctrl</kbd>+<kbd>F2</kbd>|Clear all bookmarks

## Insert mode
| Key | Description |
| --- | --- |
| **s** | delete character under cursor |
| **i** | Insert infront cursor |
| **a** | Append after cursor |
| **I** | Insert infront of line (tip: _left_ shift indicates direction) |
| **A** | Append after line end (tip: _right_ shift indicates direction) |
| **o** | Open newline below |
| **O** | Open newline above (tip: shift &#8679;) |
| **c** | Change/cut (i.e. cw = deletes word) |
| **caw** | Change/cut all word |
| **cc** | Change/cut entire line |
| **ci"** | Change inner quote content <br> (can be anywhere before for quotes, but has to be within for parenthses) |

## Selecting 
Key | Description
---|---
**v**| switch into **visual** mode
**V** | selects line (goes into **visual** mode)
**vt,** | select until the comma
**vf,** |select until with the comma
**V**_n_**gg**| select current line up to line number _n_
**V**_n_**j**| select current + down _n_ lines
<kbd>Alt</kbd> + <kbd>F3</kbd>| select all under cursor

## Undo/Redo
Key|Description
---|---
**u**|undo
<kbd>Shift</kbd> + **U**|undo all changes to current line
<kbd>&#8984;</kbd>\|\|<kbd>Ctrl</kbd> + **r**|redo
**.** | repeat last action

## Finding
Key | Description
-------|--------
**f**_x_|find _x_ and land **on** it (current line only)
**F**_x_ | Jump back on _x_ (opposite of above, current line only)
**t**_x_|'til _x_ but land **before** it (current line only)
**T**_x_ | Jump back 'til _x_ (opposite of above, current line only)
**/**|enter find
_*_|set find all word & find next
**n**|find next, alternatively using <kbd>F3</kbd>
**N**|find previous alternatively using <kbd>Shift</kbd> + <kbd>F3</kbd>
**/**|enter find
**/**|enter find
**: 3,9s/oldstring.newstring/g  s for substitude**| 
**%s/oldstring.newstring/g  s for substitude  s for substitude**| 
**%s/oldstring.newstring/gc  s for substitude**| 

## Delete/Copy/Paste
Key | Description
---|---
**d**|delete (cuts)
**dd**|delete (cuts) entire line
**D**| delete until the end of the line
**diw** | delete (& copy) entire word
**daw** | delete (& copy) entire word with trailing space
**d3w** | delete (& copy) 3 words <br> (starting from wherever cursor is)
_num_ **dd** | deletes _num_ lines
**dit**|delete inner tag content
**y**|yank (copy) selection
**yiw**|yank (copy) the current word
**yy**|yank entire line
**r**|replace single character (stays in **command** mode)
**x**|delete single character (stays in **command** mode)
**X** | delete _previous_ single character
**p**| paste after cursor
**P** |paste before cursor
**d** _num_ <kbd>Enter</kbd> | deletes _num_ lines from current position in line to current position <br> (not entire line)
**y** _num_ **p** | copies line _num_ times

## Format
Key | Description
---|---
**==**| auto-indent current line
**<<**| indent to left
**>>**| indent to right
**~**| Changes the case of current character
**gu**| Changes the selection from upper to lower
**gU**| Changes the selection from lower to upeer

# Sublime shortcuts
## General
Key | Description
---|---
<kbd>Ctrl</kbd> + **p** | Quick-open files by name
<kbd>Ctrl</kbd> + **ku** | uppercase
<kbd>Ctrl</kbd> + **kl**| lowercase
<kbd>Ctrl</kbd> + **kt**| hide (fold) all tag attributes
<kbd>Ctrl</kbd> + **k0**| expand all code
<kbd>Ctrl</kbd> + **k1**| collapse/fold all 1 tab indentations
<kbd>Ctrl</kbd> + **k2**| collapse/fold all 2 tab indentations
<kbd>Ctrl</kbd> + **kb**| toggle side bar
<kbd>Ctrl</kbd> + **kv**| paste from history
<kbd>Ctrl</kbd> + **kc**| scroll cursor to centre
<kbd>Ctrl</kbd> + **kc**| scroll cursor to centre
## Split window
Key | Description
---|---
<kbd>Shift</kbd> + <kbd>Alt</kbd> + **2** | Split view into two windows (groups)
<kbd>Ctrl</kbd> + **2** | Jump to window 2
<kbd>Shift</kbd> + <kbd>Ctrl</kbd> + **2** | Move file to group 2

