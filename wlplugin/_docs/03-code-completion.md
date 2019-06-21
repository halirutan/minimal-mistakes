---
title: "Code Completion"
permalink: /docs/code-completion/
excerpt: "Information about code completion in the Wolfram Language Plugin."
toc: false
---

IntelliJ IDEA's features for code completion work in two steps: 
1. Invoking the code completion to get a list of possible items to insert. This usually happens automatically while you
are typing but, in addition, there are several shortcuts that have special meaning.
2. Selecting and inserting and item from the code completion

## 1. Invoking Code Completion

Oftentimes, you won't have to invoke code completion manually as IntelliJ IDEA provides *auto* completion while
you are typing if you are using the default settings.
IntelliJ IDEA's behavior for code completion can be adjusted if you can go to 
**File | Settings | Editor | General | Code Completion**.
With *Show suggestions as you type** enabled, IntelliJ IDEA will automatically pop up a completion window while you are 
typing, suggesting functions that match what you have currently typed.


[![Code completion settings][1]{: .align-center}][1]

However, it is always possible to manually invoke code completion to get the popup that shows possible functions, 
symbols or expressions which can then be inserted at the current cursor position. 

- `Ctrl`+`Space` will pop up the basic code completion window.
- `Ctrl`+`Shift`+`Space` will show a *smart completion* window which only works in specific places, e.g inside the 
brackets of a built-in function, it will show the options of that function, or inside `Message[...]` it shows 
messages you have defined in your file.
- `Ctrl`+`Alt`+`Space` will show a code completion window that contains every possible symbol you have used in your code. 
- `Ctrl`+`Alt`+`T` will show possible expressions that can *surround* the current selection of code. 
That is helpful if you like to surround an expression with `Module`, braces, `Do` loops, and other things.
- The above surround completion will show a list of live templates, which are often used code constructs. This list can be accessed with . 

## 2. Inserting a completion

The completion window has basically two states: 1. No entry is focused and 2. an entry is focused.
The list will look like this

[![Code Completion not selected][2]{: .align-center}][2]

As soon as you use your arrow keys to move down the list, or you invoke the completion explicitly with one of the
shortcuts above, one entry will be highlighted. Here is the same image as above after I pressed down arrow

[![Code Completion selected][3]{: .align-center}][3]

There is not much difference between these two, except with a focused entry, you can use `[`, `(`, `;`, `Space`, and 
several other keys and the completion is inserted. If no entry is focused, insertion of the top suggestion is possible
in 3 different ways:

- pressing `Enter` simply inserts the selected entry
- pressing `Tab` will insert the entry, deleting the text that is right to the cursor. This is handy if you have mistyped something.
Let's say you have typed `AbsoluteFileName` but what you wanted was `AbsoluteTiming`.
Just go with the cursor right after the `Absolute` and start typing `T` and press `Tab`.
You see that the rest of `FileName` is replaced. 
- pressing `Ctrl`+`Shift`+`Enter` is called SmartEnter and it will insert the entry as well, but in addition, it will insert `[]`
for you if it is a built-in function.
Try typing `Ab` and press it.
The behavior if only `[]` is inserted or for instance the complete call pattern can be adjusted in 
**Settings | Languages | Mathematica**.

You can always call the completion pop up with `Ctrl`+`Space`, even in the middle of a word. As explained above, use 
`Tab` to replace the rest of the word with the current selection.

Remember, as soon as you start navigating inside the completion window and you have focused an entry, you can always 
look up its documentation with `Ctrl`+`Q` (`Cmd`+`J` on OS X).
{: .notice--info}

[1]: /assets/images/doc/03-completion-settings.png
[2]: /assets/images/doc/03-complete-not-selected.png
[3]: /assets/images/doc/03-complete-selected.png