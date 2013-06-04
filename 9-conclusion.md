# Closing Notes

**To each their own!**

## Styling

I use the [Tomorrow](https://github.com/theymaybecoders/sublime-tomorrow-theme/)
color scheme, specifically the "Night Bright" variant.

I use the [Soda Dark](https://github.com/buymeasoda/soda-theme/) theme, which
goes perfectly with "Tomorrow Night." Since I switched to the higher-contrast
"Night Bright" scheme, I've tweaked the theme to make it a little darker.

Here are my other aesthetic preferences:

    "caret_style": "smooth",
    "draw_indent_guides": true,
    "draw_minimap_border": true,
    "font_face": "Menlo",
    "font_size": 16.0,
    "highlight_line": true,
    "highlight_modified_tabs": true,
    "line_padding_top": 1

## Disabling auto-completion

I don't like the noise from having auto-completion on at all times (the
default), so I disable it:

    "auto_complete": false

As previously mentioned, I can still bring up auto-complete manually with
`⌃ + Space`.

## Showing indent guides

If you work in a lot of languages with significant whitespace (Python,
CoffeeScript, Sass...), it's easy to lose track of indentation levels. Luckily,
Sublime can draw them for you. Here are my indent guide settings, which draw
one line per level of indentation in front of the active block only:

    "draw_indent_guides": true,
    "indent_guide_options":
    [
      "draw_active"
    ]

## Paste and indent

Sublime has a handy "paste and indent" command that matches the existing
indentation when you paste code in. Since that's usually what I want to do, I
make that the default:

    { "keys": ["super+v"], "command": "paste_and_indent" },
    { "keys": ["super+shift+v"], "command": "paste" }

## Sidebar commands

I like to have a convenient key binding for toggling the sidebar:

    { "keys": ["ctrl+s"], "command": "toggle_side_bar" }

Additionally, I can use this command to see the current file in the sidebar,
opening up the folder it's in:

    { "keys": ["ctrl+super+r"], "command": "reveal_in_side_bar" }

## Playing nice with others

Before checking a file into git, it's common courtesy to:

1. Leave a blank line at the end of the file,
2. Remove trailing whitespace, and
3. Don't use tabs

You can accomplish all three of these things on every save with these prefs:

    "ensure_newline_at_eof_on_save": true,
    "trim_trailing_white_space_on_save": true,
    "translate_tabs_to_spaces": true,

## Thanks for coming!

Questions?

If you think of anything later, please raise an issue on this GitHub repo.
