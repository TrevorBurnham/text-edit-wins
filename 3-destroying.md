# Destroying

**Let's cut some cruft.**

## 1. Delete the character after the cursor

Mac keyboards have been streamlined over the years to have just the ⌫
(Backspace) key. Luckily, you can do forward-deletes using `Fn + ⌫`.

## 2. Delete a line

In any OS X GUI, you can press `⌘ + ⌫` to delete everything on a line up to the
cursor. It's equivalent to doing a ⇧-jump to the beginning of the line, then
deleting the selection.

The inverse of this is available in ST as the "Delete to End" command, bound by
default to `⌃ + K`  (which works in the shell, too).

### Challenge: Delete this line

No selection needed. ST also has a very satisfying "Delete Line" command.

## 3. Delete a word

In any OS X GUI, you can press `⌥ + ⌫` to delete everything from the cursor to
the last word boundary.  It's equivalent to doing a ⇧-jump to the last word
boundary, then deleting the selection.

## 4. Comment out code

To comment/uncomment the selected line(s) or text in Sublime, use `⌘ + /`.
