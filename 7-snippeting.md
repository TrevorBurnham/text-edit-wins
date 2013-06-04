# Snippeting

**Don't repeat yourself.**

## 1. Use a snippet from the list

Sublime Text has several snippets built in, and you can get more from packages.
To view  all available snippets for the source file you're editing, go to `Tools
-> Snippets`. (This is actually  just a shortcut for opening the Command Palette
and entering "Snippet:".)

### Pro tip: Snippet list key binding

    { "keys": ["ctrl+super+p"], "command": "show_overlay", "args": {"overlay": "command_palette", "text": "Snippet: "} }

## 2. Use a snippet from a tab binding

Snippets typically have a short abbreviation. If you place the cursor after
that abbreviation and press Tab, it will expand into the snippet.

If you use Sublime's `auto_complete`, you'll see snippet abbreviations alongside
as other completion suggestions. If you choose one of those abbreviations,
you'll get the whole snippet. Note that if you don't have `auto_complete`
enabled, you can still access it using `⌃ + space` (though this will
automatically perform the completion if there's only one).

### Challenge: Create a lorem ipsum paragraph below

lorem

## 3. Create a snippet

Snippets in Sublime are stored as files with the `.sublime-snippet` extension.
The syntax is based on TextMate. For a complete reference, see the
[snippet docs](http://docs.sublimetext.info/en/latest/reference/snippets.html).

You can store your snippets anywhere in Sublime's packages folder, but you
should use your `User` folder unless you're planning to create a new package
for your snippets.

To create a new snippet, go to `Tools -> New Snippet`.

### Pro tip: New snippet key binding

    { "keys": ["ctrl+super+n"], "command": "new_snippet"}

### Challenge: Create a snippet for console.log in JavaScript

Hints:

1. Use `<scope>source.js</scope>` to narrow the scope to JavaScript files.
2. Use `$1` to create a "field" where the cursor will be placed.
3. Use `$SELECTION` to insert the selected text
4. To insert the selected text *and* make it a field, use `${1:${SELECTION}}`.

## 4. Add a snippet key binding

You can bind a snippet to a keyboard shortcut in Sublime like so:

    { "keys": ["ctrl+alt+x"], "command": "insert_snippet", "args": {"name":
    "Packages/User/x.sublime-snippet"}}

### Challenge: Make `⌘ + B` bold selected text in Markdown

Hints:

1. `<scope>text.html.markdown.multimarkdown, text.html.markdown</scope>`
2. You bold Markdown text by **wrapping it in double-asterisks**.

