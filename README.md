# Vim Cheat Sheet

## GLOBAL

* `:help <keyword>` - Open help for keyword
* `K` - Open man page for word under the cursor

## EDITING

* `i` - Insert before the cursor (start insert mode)
* `a` - Append after the cursor
* `I` - Insert at the beginning of the line
* `A` - Append at the end of the line
* `o` - Open a new line below the current line
* `O` - Open a new line above the current line
* `r` - Replace a single character
* `R` - Replace characters from the cursor onwards (start replace mode)
* `J` - Join the current line with the next line
* `u` - Undo
* `Ctrl + r` - Redo
* `dd` - Delete (cut) the current line
* `dw` - Delete (cut) the word under the cursor
* `d$` - Delete (cut) to the end of the line
* `d^` - Delete (cut) to the beginning of the line
* `dG` - Delete (cut) to the end of the file
* `d1G` - Delete (cut) to the beginning of the file
* `cc` or `S` - Change (delete and insert) the current line
* `cw` - Change (delete and insert) the word under the cursor
* `c$` - Change (delete and insert) to the end of the line
* `c^` - Change (delete and insert) to the beginning of the line
* `C` - Change (delete and insert) to the end of the line
* `s` - Substitute (delete and insert) the character under the cursor
* `S` - Substitute (delete and insert) the current line
* `x` - Delete the character under the cursor
* `X` - Delete the character before the cursor
* `~` - Toggle the case of the character under the cursor
* `>>` - Indent the current line
* `<<` - Unindent the current line
* `:w` - Save the current file
* `:wq` or `:x` or `ZZ` - Save and close the current file
* `:q!` - Close the current file without saving
* `:e!` - Reload the current file (discard changes)
* `:e <filename>` - Open a new file in the current window
* `:sp <filename>` - Open a new file in a horizontal split window
* `:vsp <filename>` - Open a new file in a vertical split window
* `:tabnew <filename>` - Open a new file in a new tab
* `:tabs` - List open tabs
* `:tabn` or `:tabnext` - Move to the next tab
* `:tabp` or `:tabprevious` - Move to the previous tab
* `:tabclose` - Close the current tab
* `:tabonly` - Close all other tabs
* `:bufdo <command>` - Execute command on all buffers

## CURSOR MOVEMENT

* `h` - Move cursor left
* `j` - Move cursor down
* `k` - Move cursor up
* `l` - Move cursor right
* `w` - Move to the beginning of the next word
* `b` - Move to the beginning of the previous word
* `e` - Move to the end of the current word
* `0` - Move to the beginning of the line
* `$` - Move to the end of the line
* `^` - Move to the first non-blank character of the line
* `gg` - Move to the beginning of the file
* `G` - Move to the end of the file
* `<line number>G` - Move to the specified line number
* `H` - Move to the top of the screen
* `M` - Move to the middle of the screen
* `L` - Move to the bottom of the screen
* `Ctrl + f` - Move forward one screen
* `Ctrl + b` - Move backward one screen
* `Ctrl + d` - Move forward half a screen
* `Ctrl + u` - Move backward half a screen
* `%` - Jump to the matching parenthesis, bracket, or brace
* `fx` - Jump to the next occurrence of character `x` in the current line
* `tx` - Jump to the character before the next occurrence of character `x` in the current line
* `Fx` - Jump to the previous occurrence of character `x` in the current line
* `Tx` - Jump to the character after the previous occurrence of character `x` in the current line
* `;` - Repeat the last `f`, `t`, `F`, or `T` command
* `,` - Repeat the last `f`, `t`, `F`, or `T` command in the opposite direction
* `zz` - Center the current line on the screen

## CUT AND PASTE

* `yy` - Yank (copy) the current line
* `yw` - Yank (copy) the word under the cursor
* `y$` - Yank (copy) to the end of the line
* `y^` - Yank (copy) to the beginning of the line
* `yG` - Yank (copy) to the end of the file
* `y1G` - Yank (copy) to the beginning of the file
* `p` - Put (paste) the yanked or deleted text after the cursor
* `P` - Put (paste) the yanked or deleted text before the cursor
* `dd` - Delete (cut) the current line
* `dw` - Delete (cut) the word under the cursor
* `d$` - Delete (cut) to the end of the line
* `d^` - Delete (cut) to the beginning of the line
* `dG` - Delete (cut) to the end of the file
* `d1G` - Delete (cut) to the beginning of the file
* `"*p` - Paste from the system clipboard
* `"+p` - Paste from the system clipboard (alternative)
* `"*y` - Yank to the system clipboard
* `"+y` - Yank to the system clipboard (alternative)

## INDENT TEXT

* `>>` - Indent the current line
* `<<` - Unindent the current line
* `>G` - Indent to the end of the file
* `<G` - Unindent to the end of the file
* `>><number>` - Indent the next `<number>` lines
* `<<number>` - Unindent the next `<number>` lines
* `=G` - Auto-indent the entire file
* `=%` - Auto-indent the current block
* `={` - Auto-indent the current curly brace block

## SEARCH AND REPLACE

* `/pattern` - Search for `pattern` forward
* `?pattern` - Search for `pattern` backward
* `n` - Repeat the last search
* `N` - Repeat the last search in the opposite direction
* `:s/old/new/` - Replace the first occurrence of `old` with `new` in the current line
* `:s/old/new/g` - Replace all occurrences of `old` with `new` in the current line
* `:%s/old/new/g` - Replace all occurrences of `old` with `new` in the entire file
* `:%s/old/new/gc` - Replace all occurrences of `old` with `new` in the entire file with confirmation
* `:%s/\<old\>/new/g` - Replace whole words only
* `:%s/^\s\+//g` - Remove leading whitespace from all lines
* `:%s/\s\+$//g` - Remove trailing whitespace from all lines

## MARKS AND POSITIONS

* `ma` - Set mark `a` at the current position
* `'a` - Jump to the beginning of the line with mark `a`
* `` `a`` - Jump to the exact position of mark `a`
* `` ` `` - Jump to the last position before a jump
* `'.` - Jump to the last position where a change was made
* `''` - Jump to the beginning of the line where a jump was made
* `:marks` - List all marks

## REGISTERS

* `"<register>p` - Paste from register `<register>`
* `"<register>y` - Yank to register `<register>`
* `":reg` - Show all registers
* `"+p` - Paste from the system clipboard
* `"*p` - Paste from the system clipboard
* `"+y` - Yank to the system clipboard
* `"*y` - Yank to the system clipboard

## EXITING

* `:w` - Save the current file
* `:wq` or `:x` or `ZZ` - Save and close the current file
* `:q!` - Close the current file without saving
* `:e!` - Reload the current file (discard changes)

## TABS

* `:tabnew <filename>` - Open a new file in a new tab
* `:tabs` - List open tabs
* `:tabn` or `:tabnext` - Move to the next tab
* `:tabp` or `:tabprevious` - Move to the previous tab
