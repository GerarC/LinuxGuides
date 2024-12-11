# Neovim

## What is neovim?

Neovim is a modal text editor. Is a fork of vim, which in turn is the improved versión of VI. The difference between neovim and its ancestors is that it's thought to be very customizable and extensible, this is due to the fact that can be extended using LUA language by creating plugins.

## What is a Modal Text Editor?
![[glossary#^modal-text-editor]]

## Basics

### 1. How to close vim?
Anyone that has tried vim has encountered it's imposible to close it. But there's a way to exit without die. The steps are:
1. Press Escape to be sure that vim is in normal mode.
2. Press `:` to open command prompt
3. write `q!`. `q` is the command to quit vim and `!` is to do it forced just is case you made any change.

### 2. Basic usage
#### Vim modes
1. **Normal:** This is the mode of edition where you will spend the most of the time. It's the default mode when you open a file.
2. **Insert:** This mode is the unique mode that the most of the editors have, where you write your text. There are a lot of ways to access to it. But the most basic is using `i` in normal mode.
3. **Replace:** This mode overwrite anything below the cursor, you can access to it using `R` in normal mode.
4. **Visual:** Indeed, these are a family of mode to select the text, you can access to the most basic of them pressing `v` in normal mode.
5. **Terminal:** This mode can be used in a easiest way using plugin, but you can access to it writing `:term` in normal mode.

> [! Note]
> you can exit from any mode, less terminal, using `Esc`

#### Moving around the text
To move around the text you have the next possibilities:
- **Arrow keys:** these are bad options, but it still is a possibility
- **`h`, `j`, `k`, `l`:** instead of using arrow keys you can use `h` as left, `j` as down, `k` as up and `l` as right.
- **`Ctrl + y`:** this key combination downs the entire view one line.
- **`Ctrl + e`:** this key combination ups the entire view one line.
- **`Ctrl + d`:** this key combination downs half a page (`d` means down).
- **`Ctrl + u`:** this key combination ups half a page (`u` means up).
- **`Ctrl + f`:** this key combination downs a page (`f` means forward).
- **`Ctrl + b`:** this key combination ups half a page (`b` means backward).
- **`G`:** pressing `G` you can go to the end of the file.
- **`gg`:** press `g` twice sends you at the beginning of the file

With these keystrokes you can use a lot of things. For example, man pages (because it uses less), twitter, zathura, ranger, a lot of Window managers.

#### Insertion ways
As it has been said before, there are a bunch of different manners to access into insert mode:
- **`i`:** the most basic way to insert text, it places you at the left of where cursor was. `i` means insert.
- **`I`:** It places you at the beginning of the line.
- **`a`:** you can see this one as the brother of `i`, it places you at right of where cursor was. `a` means append
- **`A`:** this one places you at the end of the line.
- **`s`:** using `s` you can substitute a single letter and enter to insert mode.

#### Normal Keystrokes
In this mode there are a lot of useful keystrokes you will need and use if you want master vim:
- **`r`:** using `r`, what means replace, you can replace one character and no more.
- **`R`:** This one enters you into replace mode.
- **`u`** undo changes
- **`Ctrl + r`:** redo changes
- **`.`:** repeat the last keystroke
- **`Ctrl + y`:**

#### Advance movement ways
There are other ways to move in vim than basic, those are:
- **`0`:** moves at the beginning of the line.
- **`$`:** moves at the end of the line.
- **`^`:** moves at the beginning of the text.
- **`w`:** moves to the next word.
- **`W`:** moves to the next WORD (anything separated by spaces).
- **`b`:** moves to the previous word.
- **`B`:** goes to the previous WORD.
- **`e`:** goes at the end of the next word.
- **`E`:** move at the end of the next WORD.
- **`%`:** move between two parenthesis, curly and square braces 

#### Vim Grammar
Basically one of the best things of using vim is knowing its grammar. This one could be seen as: *Verb* + *Substantive*. where Verb is the actions you can do and Substantive text object you want to work with.

Some *Verbs* or **Actions** you can use are:
- **Yank:** using `y` you can yank text objects.
- **Delete:** using `d` you can delete/cut text objects.
- **Change:** `c` allows you to change things.

some *Substantives* or **Text Objects** that you can use are:
- **Word:** a word can be selected by using `w`.
- **WORD:** a word can be selected by using `W`.
- **Paragraph:** a paragraph can be selected by using `p`.
- **Sentence:** a sentence can be selected by using `s`.
- **() group:** parenthesis content can be selected by using `(` or `)` inside of it.
- **{} group:** curly braces content can be selected by using `{` or `}` from inside.
- **\[\] group:** square bracket can be selected by using `[` or `]` inside of it.
- **<> group:** square bracket can be selected by using `<` or `>` inside of it.
- **XML Tags:** a XML tag content can be selected using `t`.
- The same thing happens with: `"`, `'`, and \`.

To improve this even more, you can specify a little more information about the text object:
- **Inner:** if you want to select the inner information of the text object you can use `i` before the object. For example, `i(` will select anything inside the parenthesis group.
- **Around:** When you want to select around the text object you can use `a` to select it. For example, `at` should select the tag content, the tag itself and some blank space around it.

Finally, you can write how many of those Text objects you want to select. For example, `4iw` should select under the cursor and the 3 next words.


12. Macros
13. Regex aplicadas a Vim
14. Configuración básica