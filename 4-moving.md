# Moving

**Cut-and-paste is so 1982.**

## 1. Indent and unindent

You can add one level of indentation to a line by pressing `⌘ + ]`. Pressing
`⌘ + [` does the reverse.

If multiple lines are selected, all of them will move the same way.

## 2. Move a line

In Sublime Text, you can move a line up or down (i.e. swap it with its neighbor)
by holding `⌃ + ⌘` and the  appropriate arrow key.

If multiple lines are selected, all of them will move together.

### Challenge: Fix these stairs

Turn these...

    |_
          |_
      |_
        |_

into this:

    |_
      |_
        |_
          |_

## 3. Transpose chars and words

Typed two characters in the wrong order? In Sublime Text, you can put the
cursor between them and press `⌃ + T` to transpose them.

The same technique works to swap two words, too.

### Challenge: Switch the two offset values

    text-shadow: 4px 8px black;

## 4. Wrap at the ruler

Got some text that's going past your standard line length? If your ruler is set appropriately in Sublime Text, you can easily fix it using the "Wrap Paragraph at Ruler" command.

You should probably reassign that keyboard shortcut, though. Here's mine:

    { "keys": ["super+shift+\\"], "command": "wrap_lines" }

### Aside: Auto Wrap

You might want to check out the [Auto Wrap](https://github.com/randy3k/AutoWrap)
plugin. In each syntax where I don't want lines to go past the ruler (Markdown,
Git commits...),  I add these settings:

    {
      "auto_wrap": true,
      "wrap_style": "classic"
    }

## 5. Join lines

The "Join Lines" command (`⌘ + J` in ST) is essentially the opposite of the
wrap command. If multiple lines are selected, it turns them all into one line
(with a space between them). If just one line is selected, it applies to that
line and the one after it.
