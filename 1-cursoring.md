# Cursoring

**The journey begins.**

A friendly reminder:

* ⌘ = Command
* ⌃ = Control
* ⌥ = Option (a.k.a. Alt)
* ⇧ = Shift

## 1. Jump to the ends

In any OS X GUI app, you can use ⌘ with the arrow keys to jump to the end of a
line or document:

* `⌘ + ←` and `⌘ + →` jump to the beginning and end of the line
* `⌘ + ↑` and `⌘ + ↓` jump to the beginning and end of the document

## 2. Jump from word to word

In any OS X GUI app, you can use ⌥ with the left and right arrow keys to jump
from word to word:

* `⌥ + ←` jumps to the beginning of the last word
* `⌥ + →` jumps to the end of the next word

### Pro tip: Custom word separators

In Sublime Text, you can define what a "word" is by setting a `word_separators`
regex in your preferences files. The default is:

    "word_separators": "./\\()\"'-:,.;<>~!@#$%^&*|+=[]{}`~?",

Consider doing this for each language you work with by editing your preference
file for that syntax. For example, in JavaScript and CoffeeScript, `$foo` is a
valid variable name, so you might want to remove `$` from `word_separators`.

## 3. (Advanced) Jump from subword to subword

If you often finding yourself editing variablesThatAreNamedLikeThis, or
variables_that_are_named_like_this, you might  want to add a key binding for
jumping between "subwords." In Sublime Text, you  can do that by going to your
key bindings (`Key Bindings - User`, available  via the Command Palette) and
adding this:

    { "keys": ["ctrl+alt+left"], "command": "move", "args": {"by": "subwords", "forward": false} },
    { "keys": ["ctrl+alt+right"], "command": "move", "args": {"by": "subword_ends", "forward": true} },
    { "keys": ["ctrl+alt+shift+left"], "command": "move", "args": {"by": "subwords", "forward": false, "extend": true} },
    { "keys": ["ctrl+alt+shift+right"], "command": "move", "args": {"by": "subword_ends", "forward": true, "extend": true} },

Now `⌃ + ⌥` works with the left and right arrows to move between parts of
camelCased or underscore_delimited words.

## 4. (Advanced) Jump from paragraph to paragraph

`⌥ + ↑` and `⌥ + ↓` don't do anything special in OS X. What a waste! You can
bind those keys in Sublime to jump from one paragraph to another (or more
precisely, from one blank line to another). This also makes it very easy to
select entire paragraphs:

    {"keys": ["alt+up"], "command": "move", "args": {"by": "stops", "empty_line": true, "forward": false}},
    {"keys": ["alt+down"], "command": "move", "args": {"by": "stops", "empty_line": true, "forward": true}},
    {"keys": ["shift+alt+up"], "command": "move", "args": {"by": "stops", "empty_line": true, "forward": false, "extend": true}},
    {"keys": ["shift+alt+down"], "command": "move", "args": {"by": "stops", "empty_line": true, "forward": true, "extend": true}},

## 5. Jump from page to page

To move the cursor to the previous/next "page," use `Fn + ↑` and `Fn + ↓` on
your slender `Page Up`/`Page Down`-free Apple keyboard.

## 6. (Advanced) Multi-cursoring

In Sublime Text, you can have multiple cursors at the same time. The most
direct way to create multiple cursors is to `⌘ + click` in each place you want
one. To go back to one cursor, press ⎋ (Escape).

We'll see more ways to create multiple cursors in the "Multi-select" section.

(Vim users: Check out
[vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors).)

### Challenge: Fill any diagonal of this tic-tac-toe board with x's

    [ ] [ ] [ ]
    [ ] [ ] [ ]
    [ ] [ ] [ ]
