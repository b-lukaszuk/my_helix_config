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
