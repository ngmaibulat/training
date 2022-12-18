### VIM Basics

```bash
sudo apt install vim
vim filename.sh
bash filename.sh
```

### Tabbed Edit

```bash
vim -p file1.txt file2.txt
```

```
gt - move to the next tab
gT - move to the previous tab
```

### Split screen, make windows

```
:vsp [filename] - Open file, split screen: side by side
:sp [filename] - Open file, split screen, one of top of another
:ls - Lists all open buffers

Ctrl + ws - split screen horizontally for same file
Ctrl + wv - split screen vertically for same file

Ctrl + ww - Switch between windows
Ctrl + wq - Quit a window

Ctrl + wh - Switch to right window
Ctrl + wl - Switch to left window
Ctrl + wj - Switch to below window
Ctrl + wk - Switch to upper windows
```

### Move cursor

```
h - Move left
l - Move right
j - Move down
k - Move up
```

```
5k - Move up, 5 times
10k - Move up, 10 times
```

```
H - Move to top of the screen
M - Move to middle of the screen
L - Move to bottom of the screen

w - Move to start of the next word
b - Move to start of the previous word
e - Move to end of a word

0 - Move to beginning of a line
$ - Move to end of a line

) - Move to next sentence
( - Move to previous sentence
} - Move to next paragraph
{ - Move to previous paragraph
```

```
gg - Places the cursor at the start of the file
G - Places the cursor at the end of the file
```

### Vim commands for editing

```
yy - Copies a line
yw - Copies a word
y$ - Copies from where your cursor is to the end of a line
5yy - Copy 5 lines
```

```
v - Highlight one character, use arrow keys
V - Highlights one line, use arrow keys
```

```
p - Paste
u - Undo
```

```
d - Deletes highlighted text
dd - Deletes a line of text
dw - Deletes a word

D - Delete from cursor to the end of line
d0 - Delete from beginning of line to the cursor
dgg - Deletes from beginning to the end
dG - Delete from cursor to the end
```

```
rs - change current character to 's'
x - Deletes a single character
u - Undo
Ctrl + r - Redo the last undo
. - Repeats the last action
```

### Search

```
/str - search for text
/^str - searh for text in begining of each line
/str$ - search for text in the end of each line

n - go to next search result
N - go to prev search result

* - search for current word
# - search for current word, backward

:nohl - remove high-lighting
```

Search history:

```
type /
use arrow keys
```

### Replace

```
:s/[pattern]/[replacement]/g - Replace on current line only
:%s/[pattern]/[replacement]/g - Replace, no confirm
:%s/[pattern]/[replacement]/gc - Replace, ask for confirmation
```

### Marking text

```
v - visual mode, select from current character
V - visual mode, select lines

Ctrl + v - starts visual block mode (selects columns)

Ctrl + v ab - select block with ()
Ctrl + v aB - a block with {}

Ctrl + v ib - select inner block with ()
Ctrl + v iB - select inner block with {}

vaw - mark a word

Esc - exit visual mode
```

### With selected text:

```
d - delete marked text
y - yank (copy) marked text
> - shift text right
< - shift text left
~ - swap case
```

### Run shell commands:

```
:!cmd - run cmd
:!ls  - run ls

:shell - open shell, return to vim after exit

:terminal - open terminal as window
```
