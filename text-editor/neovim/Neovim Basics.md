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
- **`o`:** pressing `o`, vim opens a new line below the current line and places you in there.
- **`O`:** The same utility of its lowercase, but `O` open a new line above the current line.

#### Normal Keystrokes
In this mode there are a lot of useful keystrokes you will need and use if you want master vim:
- **`r`:** using `r`, what means replace, you can replace one character and no more.
- **`R`:** This one enters you into replace mode.
- **`u`** undo changes
- **`Ctrl + r`:** redo changes
- **`.`:** repeat the last keystroke
- **`Ctrl + y`:**
- **`p`:** paste just in of the cursor
- **`P`:** paste before the cursor

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
Basically one of the best things of using vim is knowing its grammar. This one could be seen as: *Verb* + *Substantive*. where Verb is the actions you can do and Substantive is a text object or selection you want to work with.

Some *Verbs* or **Actions** you can use are:
- **Yank:** using `y` you can yank text objects.
- **Delete:** using `d` you can delete/cut text objects.
- **Change:** `c` allows you to change things.

some **Text Objects** that you can use are:
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

To improve text objects even more, you can specify a little more information about the text object:
- **Inner:** if you want to select the inner information of the text object you can use `i` before the object. For example, `i(` will select anything inside the parenthesis group.
- **Around:** When you want to select around the text object you can use `a` to select it. For example, `at` should select the tag content, the tag itself and some blank space around it.

Some **Selections** you can do are:
- **Find:** you can select all the content in the line between the cursor and the next character you indicates using `f`. For example, if you have *There's going to happen something good*, the cursor is above the *r* and press `dfp`, Vim will delete from the *r* to the first *p* it find, including it. `F` do the same but with text before the cursor. You can move between founded chars using  `,` and `;`.
- **'Til:** this basically the same of the find but without selecting the character you put. This is using `t`, to search forwards and `T` to search backwards. You can move as using find.
- **Search:** you can use `/` to search words and regex, you can use that selection after indicate an action to use as selection mode. You can move between coincidences using `n`and `N`.
- **Backward searching:** as the searching mode, you can use `?` to search and select backwards. Also you can move between coincidences using `n` and `N`

Finally, you can write how many of these *Verbs* you want to select. For example, `4iw` should select under the cursor and the 3 next words.

#### Utils
1. You can select and search a Word already exists using `#` and `*`, Also you can move between coincidences using both keys, `#` to move backwards and `*` to move forward.

#### Macros
A macro is basically record a series of keystrokes and save it in memory. to start to record a macro you can use `q<char>` in normal mode where `<char>` is any key where you want to save your macro. And when you want to apply it, you can write `@<char>` in visual or normal mode.

### 3. Regex apply to Vim
Using Regex is one of the best utilities of Vim. This can be applied to searching and substitute.

> [! CAUTION] Note
> As this is not a REGEX tutorial, I'm going to suggest U to explore it in [Regular Expressions 101](https://regex101.com/). 

#### Regex basics
As I've just said this is not a Regex tutorial, But I'd rather explain a bit of it.

Regular expressions basically allows you to represent a pattern of characters easily. There are the most basic of then:
- **Any Character or Word:** if you want to search a single one character you can use that character, for example `a`, it will match any *a*, also you can seek for `word`, It will match anytime *word* appears.
- **Group of characters:** Using square brackets you can define a group of characters you want to match. For example, `[aiueo]` will match any vocal, and it doesn't take the order, just the characters inside.
- **Grouping matches:** you can group matches using parenthesis, this is very useful when you want to substitute something. For example, `(k[aiueo])` will match and make a group of *ka*, *ki*, *ku*, *ke*, *ko*.
- **Common RegEx Symbols:** regex has a lot of symbols used to represent types of characters, but these are the most common:
	- `.`: A do means any character.
	- `+`: plus sign means that the previous character or group should appear one or more times in a row.
	- `*`: asterisk mean that the previous match should appear zero or more times in a row.
	-`?`: a question mark means that the previous match must appear once or not appear.
- **Escaping characters:** finally if you want to match any special character you can use a `\`before it. It also is commonly used to represent some groups. For example, `\w` represents any word character.

#### Using regex to search
Now, knowing a little then you can use it to search strings. To illustrate it, if you wanna search any XML tag in a text, you can use `/<.*>`

#### Regex to substitute
This is one of the most powerful things Vim has, you can use some `sed` functionalities to edit text inside the program. And the most commonly used is `s` or substitution.

The format of substitution is `<range>s/<pattern>/<substitute>/<flags>`. Let's explain each one:
- `<range>`: this is the range that can take the command, you can specify a range of lines writing `<n1>,<n2>`, where `<n1>` and`<n2>` are the first line of the range and the final respectively; a visual selection using `'<,'>` though it places automatically if you are in visual mode, the entire file putting `%` or just the current line with `.`.
- `<pattern>`: this is the regex pattern to match the substitution candidate.
- `<substitute>`: is the string that will replace the matched pattern.
- `<flags>`: is where you place flags if you need some of them. Some of the flags are: `g` to substitute any match and not only the first of the line, `i` is to ignore the case, and `I` is to take in account letters case.

##### Explanation Cases
1. you have the text *murcielago*, and you use `:s/[aiueo]/_/g` it will replace any vocal with *_* so, the result is *m_rc__l_g_*.
2. As was said, you can make groups with `()`, then you can use it to substitute something and reuse it in the result. For example, you have the text *hola amigos mios*, so you can use `:s/hola \(amigos\)/adios "\1"/g`. Here you have to escape parenthesis, and each group you catch, you can use it escaping its index, starting with 1. The result it's going to be *adios "amigos" mios*.
