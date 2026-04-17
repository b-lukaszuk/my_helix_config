# Some notes about Helix editor

## Mode: Normal

`:tutor` - to start the built-in tutorial

### Moves

`h`, `j`, `k`, `l` - standard Vim like motions (left, down, up, right)

- `d` - deletes the character under the cursor (or what's currently marked)
- `c` - changes the character under the cursor (or what's currently marked)
- `w` - select forward until the next word

overall, it works based on object - action combinations
(changing/adding muscle memory to Vim like keybindings may be painful)

- `v` - visual mode, extends currenttly marked text on which you may perform a given operation
- `x` - selects the whole line, each consecutive 'x' press repeats the operation
- `;` - colapses selection(s) to (a) single cursor(s).

### Undo/redo

- `u` - undo
- `U` - redo

### Copy/paste

- `y` - yank (copy) the selection
- `p`/`P` - paste the yanked selection after/before the cursor

### Search in file

- like in Vim: `/` and `?`
- `n` and `N` - but `n` always moves forwards, and `N` always moves backwards
- `gw` - like avy-goto-char2 in Emacs

by default search goes to register `/`, `*` copies lecection into register `/`

### Multiple Cursors

- `C` - duplicates cursor to the next suitable line.
- `,` - removes the first cursor (or first n cursors) of the two (or of x cursors)
- `s` - selection (regex and regular) within a selection (also replace with `c`)
- `x` select whatever, and `%` select whole file

### Repetition

- `.` - repeats the last insert command
- `Alt-.` - repeats the last `f`/`t` selection

### Replace

- `r` replaces selection with a character
- `R` replaces the selection with previously yanked text

### Increment and decrement

- `Ctrl-a` - increments number under selection
- `Ctrl-x` - decrements number under selection

### Macros

- `Q` - start/end recording a macro (by default goes to register `@`)
- `q` - repeat the macro from register `@`

### Changing case

- `~` switch case
- `` ` `` - switch to lowercase
- `` Alt-` `` - switch to uppercase

### Comments

- `Ctrl-c` - toggle comment/uncomment

### Match mode

- `m` - while standing on `(`, `[` or `{` moves to the match (back and forth)
- `mi` and `(`, `[` or `{` marks contents of parenthesis
- `ma` and `(`, `[` or `{` marks contents of parenthesis with them
- `m(`, etc. - surround marked text with parentheses
- `md(`, etc. - deletes parentheses around marked text
- `mr([`, etc. replaces `()` with `[]`

### Windows

- `C-w` - opens a submenu that allows to do stuff with windows

Quite a few of `C-w` commands are like in Vim.

- `C-w nv` - opens scratch buffer in vertical split
- `C-w ns` - opens scratch buffer in horizontal split
- `:vs buffer_or_file_to_open` - opens a buffer or file in vertical split
- `:hs buffer_or_file_to_open` -  opens a buffer or file in horizontal split
- `C-w t` - two way transpose between vertical and horizontal split
- `C-w K`/`C-w J` - swap with window above/below
- `C-w H`/`C-w L` - swap with window on the left/right

While in file picker (`space f`) press `Enter` to open file in current window
or `C-v`/`C-s` to open it in new vertical/horizontal split

- `C-w o` - close all other splits except currently active window
- `C-w q` - close current window

### Gotos

- `gg`/`ge` - goto beginning/end of file
- `gh`/`gl` - goto beginning/end of line
