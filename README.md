Custom Cocoa Text System Key Bindings
===
The Cocoa Text System allows you to map arbitrary sequences of text commands to keyboard shortcuts, giving you custom text keybindings that will work in any Cocoa text field, not just your text editor of choice.

Usage
---
Replace each instance of `[keybinding]` with the keyboard shortcut you’d like to use for the command. Use `@` for `⌘`, `~` for `⌥`, and `^` for `⌃`. Place `DefaultKeyBinding.dict` in `~/Library/KeyBindings` and restart each application for the keybindings to take effect.

To use these keybindings within Xcode requires a second representation of each keybinding to be included in `/Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Versions/A/Resources/IDETextKeyBindingSet.plist`. These are in the form of key-value pairs, with the name as the key and a comma separated list of selectors as the string value. I added these in a separate “Custom Bindings” section; the template for this section is provided below. The actual keyboard shortcuts used will mirror those defined in `~/Library/KeyBindings/DefaultKeyBinding.dict`.

Commands
---
* __Select Next Word__ — Selects the next word in the document, starting with the one under the cursor. Repeated application selects each subsequent word.
* __Select Next Line__ — Selects the next line in the document, starting with the one under the cursor. Repeated application selects each subsequent line.
* __Move Line Up__ — Switches the current line (selected line or line under the cursor) with the line above.
* __Move Line Down__ — Switches the current line with the line below.
* __Duplicate Line__ — Inserts a copy of the current line below that line.
* __Clear Line__ — Replaces the current line with an empty line.
* __Delete Line__ — Removes the current line.
* __Shrink Selection__ — Moves the starting point of the selection forward one character and the ending point backward one character. For use with Xcode’s “Balance Delimiters” command; will change a selection between two delimiters (inclusive) to one exclusive.
* __Move to Opening Brace from Selection__ — For use with Xcode’s “Balance Delimiters” command; move the cursor to immediately after the opening brace for the current selection or cursor position.
* __Move to Closing Brace from Selection__ — For use with Xcode’s “Balance Delimiters” command; move the cursor to immediately before the closing brace for the current selection or cursor position.
