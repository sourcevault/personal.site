---
title: "Vim Commands"
date: "2023-06-28"
tags: [
    "repetitive strain injury",
    "keyboard",
    "KRepublic.com",
    "ergonomics"
    ]
author: "sourcevault"
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: true
hidemeta: false
comments: false
# description:
# disableHLJS: false # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: false

---

## *VIM commands*
| description | command |
| --- | --- |
| open help for keyword                   | :h keyword |
| save file as                            | :sav file |
| close current pane                      | :clo |
| open a terminal window                  | :ter |
| open man page for word under the cursor | K |
#### Cursor movement
| description | command |
| --- | --- |
| move cursor left                      | h |
| move cursor down                      | j |
| move cursor up                        | k |
| move cursor right                     | l |
| move to top of screen                 | H |
| move to middle of screen              | M |
| move to bottom of screen              | L |

| description | command |
| --- | --- |
| jump forwards to the start of a word  | w |
| jump forwards to the end of a word    | e |
| jump backwards to the start of a word | b |
| jump to the start of the line         | 0 |
| jump to the end of the line           | $ |
| go to the first line of the document  | gg |
| go to the last line of the document   | G |
| go to line 5                          | 5gg |
| repeat previous f, t, F or T movement | ; |
| center cursor on screen               | zz |
| move back one full screen             | ctrl + b |
| move forward one full screen          | ctrl + f |
| move forward 1/2 a screen             | ctrl + d |
| move back 1/2 a screen                | ctrl + u |

| description | command |
| --- | --- |
| jump to next occurrence of character x            | fx |
| jump to before next occurrence of character x     | tx |
| jump to previous occurence of character x         | Fx |
| jump to the first non-blank character of the line | ^ |
| jump to after previous occurence of character x   | Tx |
| move screen up one line (without moving cursor)   | ctrl + y |
| repeat previous f, t, F or T movement, backwards  | , |
| move screen down one line (without moving cursor) | ctrl + e |
| jump to the last non-blank character of the line  | g_ |

| description | command |
| --- | --- |
| jump to next paragraph (or function/block, when editing code)         | } |
| jump to previous paragraph (or function/block, when editing code)     | { |
| jump forwards to the start of a word (words can contain punctuation)  | W |
| jump forwards to the end of a word (words can contain punctuation)    | E |
| jump backwards to the start of a word (words can contain punctuation) | B |
| move to matching character (default supported pairs: '()', '{}', '[]' - use :h matchpairs in vim for more info) | % |
#### Insert mode
| description | command |
| --- | --- |
| insert before the cursor                                  | i        |
| insert at the beginning of the line                       | I        |
| insert (append) after the cursor                          | a        |
| insert (append) at the end of the line                    | A        |
| append (open) a new line below the current line           | o        |
| append (open) a new line above the current line           | O        |
| insert (append) at the end of the word                    | ea       |
| delete the character before the cursor during insert mode | ctrl + h |
| delete word before the cursor during insert mode          | ctrl + w |
| list of marks                                      | :marks   |
| set current position for mark A                    | ma       |
| jump to position of mark A                         | `a       |
| yank text to position of mark A                    | y`a      |
| go to the position where Vim was previously exited | `0       |
| go to the position when last editing this file     | `"       |
| go to the position of the last change in this file | `.       |
| go to the position before the last jump            | ``       |
| list of jumps                                      | :ju      |
| go to newer position in jump list                  | ctrl + i |
| go to older position in jump list                  | ctrl + o |
| list of changes                                    | :changes |
| go to newer position in change list                | g,       |
| go to older position in change list                | g;       |
| jump to the tag under cursor                       | ctrl + ] |
#### Macros
| description | command |
| --- | --- |
| record macro a       | qa |
| stop recording macro | q  |
| run macro a          | @a |
| rerun last run macro | @@ |
#### Cut and paste
| description | command |
| --- | --- |
| yank (copy) a line                                                                            | yy  |
| yank (copy) 2 lines                                                                           | 2yy |
| yank (copy) the characters of the word from the cursor position to the start of the next word | yw  |
| yank (copy) to end of line                                                                    | y$  |
| put (paste) the clipboard after cursor                                                        | p   |
| put (paste) before cursor                                                                     | P   |
| start visual mode, mark lines, then do a command (like y-yank)                                | v   |
| start linewise visual mode                                                                    | V   |
| move to other end of marked area                                                              | o   |
| start visual block mode       | ctrl + v |
| move to other corner of block | O        |
| mark a word                   | aw       |
| a block with ()               | ab       |
| a block with {}               | aB       |
| a block with <> tags          | at       |
| inner block with ()           | ib       |
| inner block with {}           | iB       |
| inner block with <> tags      | it       |
| exit visual mode              | esc      |
#### Visual commands
| description | command |
| --- | --- |
| shift text right                | > |
| shift text left                 | < |
| yank (copy) marked text         | y |
| delete marked text              | d |
| switch case                     | ~ |
| change marked text to lowercase | u |
| change marked text to uppercase | U |
#### Registers
| description | command |
| --- | --- |
| show registers content                                                     | :reg     |
| yank into register x                                                       | "xy      |
| paste contents of register x                                               | "xp      |
| yank into the system clipboard register                                    | "+y      |
| paste from the system clipboard register                                   | "+p      |
| begin new line during insert mode                                          | ctrl + j |
| indent (move right) line one shiftwidth during insert mode                 | ctrl + t |
| de-indent (move left) line one shiftwidth during insert mode               | ctrl + d |
| insert (auto-complete) next match before the cursor during insert mode     | ctrl + n |
| insert (auto-complete) previous match before the cursor during insert mode | ctrl + p |
| exit insert mode                                                           | esc      |
#### Editing
| description | command |
| --- | --- |
| replace a single character                                   | r    |
| join line below to the current one with one space in between | J    |
| join line below to the current one without space in between  | gJ   |
| reflow paragraph                                             | gwip |
| switch case up to motion                                     | g~   |
| change to lowercase up to motion                             | gu   |
| change to uppercase up to motion                             | gU   |
| change (replace) entire line                                 | cc   |
| change (replace) to the end of the line                      | C    |
| change (replace) to the end of the line                      | c$   |
| change (replace) entire word                                 | ciw  |
| change (replace) to the end of the word      | cw       |
| delete character and substitute text         | s        |
| delete line and substitute text (same as cc) | S        |
| transpose two letters (delete and paste)     | xp       |
| undo                                         | u        |
| restore (undo) last changed line             | U        |
| redo                                         | ctrl + r |
| repeat last command                          | .        |
| open all folds at the cursor                 | zO       |
| close fold under the cursor                  | zc       |
| reduce (open) all folds by one level         | zr       |
| open all folds                               | zR       |
| fold more (close) all folds by one level     | zm       |
| close all open folds                         | zM       |
| delete all folds                             | zE       |
| toggle folding functionality                       | zi          |
| move to start of open fold.                        | [z          |
| move to end of open fold.                          | ]z          |
| make all windows equal height & width              | ctrl + w  = |
| move cursor to the left window (vertical split)    | ctrl + w  h |
| move cursor to the right window (vertical split)   | ctrl + w  l |
| move cursor to the window below (horizontal split) | ctrl + w  j |
| move cursor to the window above (horizontal split) | ctrl + w  k |
#### Tabs
| description | command |
| --- | --- |
| open a file in a new tab                                             | :tabnew        |
| move the current split window into its own tab                       | ctrl + w  t    |
| move to the next tab                                                 | gt             |
| move to the previous tab                                             | gT             |
| move to tab number #                                                 | #gt            |
| move current tab to the #th position (indexed from 0)                | :tabm #        |
| close the current tab and all its windows                            | :tabc          |
| close all tabs except for the current one                            | :tabo          |
| run the command on all tabs (e.g. :tabdo q - closes all opened tabs) | :tabdo command | 
#### Diff
| description | command |
| --- | --- |
| jump to start of next change                                         | ]c             |
| jump to start of previous change                                     | [c             |
| obtain (get) difference (from other buffer)                          | do             |
| put difference (to other buffer)                                     | dp             |
| make current window part of diff                                     | :diffthis      |
| update differences|:dif |
| switch off diff mode for current window|:diffo |
#### Folding
| description | command |
| --- | --- |
| manually define a fold up to motion                                            | zf                 |
| delete fold under the cursor                                                   | zd                 |
| toggle fold under the cursor                                                   | za                 |
| open fold under the cursor                                                     | zo                 |
| repeat search in same direction                                                | n                  |
| repeat search in opposite direction                                            | N                  |
| replace all old with new throughout file                                       | :%s/old/new/g      |
| replace all old with new throughout file with confirmations                    | :%s/old/new/gc     |
| remove highlighting of search matches                                          | :noh               |
| search for pattern 'foo' in all .js files in every sub-directory (recursively) | :vim /foo/ **/*.js |
| jump to the next match                                                         | :cn                |
| jump to the previous match                                                     | :cp                |
| open a window containing the list of matches                                   | :cope              |
| edit a file in a new buffer                             | :e file     |
| go to the next buffer                                   | :bn         |
| go to the previous buffer                               | :bp         |
| delete a buffer (close a file)                          | :bd         |
| go to a buffer by #                                     | :b#         |
| go to a buffer by file                                  | :b file     |
| list all open buffers                                   | :ls         |
| open a file in a new buffer and split window            | :sp file    |
| open a file in a new buffer and vertically split window | :vs file    |
| edit all buffers as vertical windows                    | :vert ba    |
| edit all buffers as tabs                                | :tab ba     |
| split window                                            | ctrl + w  s |
| split window vertically                                 | ctrl + w  v |
| switch windows                                          | ctrl + w  w |
| quit a window                                           | ctrl + w  q |
| exchange current window with next one                                                          | ctrl + w  x |
| delete (cut) a line                                                                            | dd          |
| delete (cut) 2 lines                                                                           | 2dd         |
| delete (cut) the characters of the word from the cursor position to the start of the next word | dw          |
| delete (cut) to the end of the line | D  |
| delete (cut) to the end of the line | d$ |
| delete (cut) character              | x  |
#### Indent text
| description | command |
| --- | --- |
| indent (move right) line one shiftwidth        | >>  |
| de-indent (move left) line one shiftwidth      | <<  |
| indent a block with () or {} (cursor on brace) | >%  |
| indent inner block with ()                     | >ib |
| indent a block with <> tags                       | >at |
| re-indent 3 lines                                 | 3== |
| re-indent a block with () or {} (cursor on brace) | =%  |
| re-indent inner block with {}                     | =iB |
| re-indent entire buffer | gg=G |
| paste and adjust indent to current line| ]p |
#### Exiting
| description | command |
| --- | --- |
| write (save) the file, but don't exit|:w |
| write out the current file using sudo     | :w !sudo tee % |
| write (save) and quit                     | :wq            |
| quit (fails if there are unsaved changes) | :q             |
| quit and throw away unsaved changes       | :q!            |
| write (save) and quit on all tabs|:wqa|
#### Search and replace
| description | command |
| --- | --- |
| search for pattern                                                                               | /pattern  |
| search backward for pattern                                                                      | ?pattern  |
| search for 'very magic' pattern (auto-interpret non-alphanumeric chars as special regex symbols) | \vpattern |


