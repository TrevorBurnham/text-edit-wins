# Plugins

Miscellaneous goodness that didn't fit anywhere else.

I'm assuming that if you use Sublime Text, you use
[Package Control](http://wbond.net/sublime_packages/package_control).

## SublimeLinter

This was plugged by Paul Irish as a tool that's radically changed the way he
works. Essentially, it tells you whenever you make a syntax mistake, using the
appropriate linter for the language you're working in.

It does require some configuration. After installing, use the Command Palette
to open both "SublimeLinter Settings - Default" (for reference) and
"SublimeLinter Settings - User." For a start, I recommend setting it to lint
only on save to reduce noise:

    "sublimelinter": "load-save"

See the [SublimeLinter README](https://github.com/SublimeLinter/SublimeLinter)
for complete documentation.

## Git

This packages gives you access to all kinds of git commands via Sublime's
Command Palette. Plus, it gives you syntax highlighting for git commit messages,
which is an absolute treat.

My favorite trick with this plugin: If you've gotten carried away and made a
bunch of changes to a file but you want to keep your commits fine-grained, just
select the lines you want to commit and use the "Git: Add Selected Hunk"
command to stage them for your next commit.

## GitGutter

[GitGutter](https://github.com/jisaacks/GitGutter) shows you in real-time what's
changed relative to your last commit.

## Browser Refresh

Tabbing back and forth between your editor and your browser when you make
changes can be a pain. One solution is to set up a tool like
[LiveReload](http://livereload.com/) to watch the directory your editing and
refresh your browser when changes are detected. A simpler solution is to
use the [Browser Refresh](https://github.com/gcollazo/BrowserRefresh-Sublime)
plugin, which lets you save and refresh your active browser tab with a single
keystroke.

After installing, you need to set up a key binding. Here's mine:

    {
      "keys": ["super+shift+r"], "command": "browser_refresh", "args": {
        "auto_save": true,
        "delay": 0.0,
        "activate_browser": false,
        "browser_name" : "Google Chrome"
      }
    },

## Emmet

Formerly known as Zen Coding, and available for all major text editors. So
amazing that it deserves its own file...
