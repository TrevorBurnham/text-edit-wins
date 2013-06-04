# Selecting

**Skip the click-and-drag.**

## 1. Jump ‘n’ select

In any OS X GUI, you can press ⇧ while doing any of the jumps we talked about in
"Cursoring" to select everything between the cursor and its new location.

### Challenge: Select this line

You can ⇧-jump from either end. In ST, you might also try `⌘ + L`.

### Challenge: Select a word in this line

The quick brown fox jumps over the... psst, in ST, try `⌘ + D`.

## 2. (Advanced) Multi-select

In Sublime Text, you can click and drag while holding ⌘ to add new selection
areas as well as new cursors.

Another way to do multi-selection in ST is borrowed from TextMate: *column
selection.* Just hold ⌥ while dragging to select rectangular areas of text.
Each line of text is treated as a separate selection.

We'll learn one more way to do multi-selection in the "Selecting word instances"
section.

### Challenge: Select the W only

     __       __   _______   __    __
    |  \  _  |  \ |       \ |  \  |  \
    | $$ / \ | $$  \$$$$$$$ | $$\ | $$
    | $$/  $\| $$   | $$$   | $$$\| $$
    | $$  $$$\ $$   | $$$   | $$$$\ $$
    | $$ $$\$$\$$   | $$$   | $$\$$ $$
    | $$$$  \$$$$  _| $$$_  | $$ \$$$$
    | $$$    \$$$ |   $$$ \ | $$  \$$$
     \$$      \$$  \$$$$$$$  \$$   \$$

## 3. (Advanced) Expand selection

Sublime Text has various "Expand Selection" commands. Among the most useful
are:

* **...to Word:** Everything between two word boundaries
* **...to Indentation:** Everything adjacent with the same indentation level
* **...to Brackets:** Everything inside of matching brackets (parens, etc.)
* **...to Tag:** Everything inside of matching HTML tags

### Challenge: Select the argument list, and the function body

    function makeOmelette(eggs, cheese, banana) {
      // Legacy code in case someone attempts to pass a banana
      if (banana) throw new Error('wut?');
    }

### Challenge: Select the heading text

<h3>Welcome to the Wonderful World of Win!</h3>

### Bonus: Expand selection to quotes

Sublime doesn't come with an "Expand Selection to Quotes" command out of the
box, but you can get one via
[this plugin](https://github.com/kek/sublime-expand-selection-to-quotes).
It binds the command to `⌃ + '` by default.

## 4. (Advanced) Selecting word instances

In Sublime Text, the "Expand Selection to Word" command serves a dual purpose.
If there's already a selection, it will select the next instance of that
text--*while preserving the existing selection.*

Technically, this is a separate command ("Quick Add Next") bound to the same
keyboard combination.

### Challenge: Turn the puppies into kitties without find & replace

    puppies puppies puppies puppies puppies puppies puppies
