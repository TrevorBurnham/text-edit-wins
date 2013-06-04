# Finding

**An epic quest to fetch some text.**

## 1. Use selection for find

In any OS X GUI app, you can use `⌘ + E` to set the thing you want to find.
This works across applications. Consider this 4-step process:

1. `⌘ + C` to copy what you want to find
2. `⌘ + F` to bring up the find dialog
3. `⌘ + V` to paste
4. `Enter`

With this trick, you can cut it in half:

1. `⌘ + E` to use selection for find
2. `⌘ + G` to "Find Next"

### Aside: Word select and find

As we saw in "Selecting word instances," the "Quick Add Next" command (`⌘ + D`)
is a great way to select additional instances of selected text. Because it's a
pseudo-find operation, the selection is set as the "Find" text automatically.
It's as if `⌘ + D` presses `⌘ + E` for you.

## 2. Quick find

Without bringing up the Find dialog, you can use `⌥ + ⌘ + G` to take the current
selection (or the word the cursor is on) and select the next instance.

It's just like `⌘ + D`, except that it loses the existing selection.

## 3. Quick find all

If you want to select every instance of some text in a file without tapping
`⌘ + D` a  gazillion times, select what you want and use the "Quick Find All"
command.

## 4. Project-wide find

You can find across all open files (that is, all files that are in the sidebar
plus any files that are in open tabs) using Sublime's "Find in Files" command.

"Find in Files" is a common source of confusion to Sublime newcomers, because
the results appear as a normal-looking text document in a new tab. Here are
the most important things to know:

1. You can jump to a search result by double-clicking the matching text.
2. "Find in Files" incorporates *unsaved changes* you've made.
3. You can use the '...' next to "Where" to narrow down the search area.

## 5. (Advanced) Incremental find

Sublime's "Incremental Find" command (`⌘ + I`) is a variant of the Find dialog
with a few subtly different behaviors.

Incremental Find instantly takes you to the first instance of whatever you
type, as you type it. If you press Enter, you'll stay there. If you press Esc,
you'll go back to where you were before.

You can tap `⌘ + I` repeatedly to cycle through matches.

Basically, Incremental Find is a quick way of looking for something else in the
document without losing your place.

## 6. (Advanced) Quick skip next

Here's a tricky one. What if you want to select some instances of something
but skip over others? Sublime implements this with a hidden "Quick Skip Next"
command.

Here's how it works: Press `⌘ + K` after each selection you don't want. It'll
be deselected when you make the next selection with `⌘ + D`.

Unfortunately, there's no visual confirmation when you hit `⌘ + K`, making it
very easy to make mistakes with this technique. You might want to check out the
[SuperSelect](https://github.com/codecarson/SublimeSuperSelect) plugin for a
more robust solution.

### Challenge: Select the first, third, and last hamster

    hamster hamster hamster hamster hamster
