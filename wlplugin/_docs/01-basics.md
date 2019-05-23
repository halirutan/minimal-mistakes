---
title: "Basic Usage"
permalink: /docs/basics/
excerpt: "Basic usage of the Wolfram Language Plugin"
toc: false
---

All features are directly incorporated into the IntelliJ IDE.
Therefore, by familiarizing yourself with IntelliJ IDEA you will automatically know how to use the plugin for Wolfram
 Language code, because it works consistently for all 
programming languages.
You will find a lot of documentation on [the official Jetbrains site](https://www.jetbrains.com/idea/documentation/), but to get a quick start, I suggest the following

* Read through the [Quick Start](https://www.jetbrains.com/help/idea/discover-intellij-idea.html) you find in the official documentation
* Skim at least once through the [Keymap Shortcuts](http://www.jetbrains.com/idea/docs/IntelliJIDEA_ReferenceCard.pdf)
* Click some minutes trough the _Tip of the Day_ dialog which shows up when you open IDEA or click on **Help | Tip of
 the Day**
 

Before reading further, let me emphasize that if you want to turn this into the ultimate experience, you have to engage 
with the way IntelliJ IDEA works.
This means that you have to refer to the shortcut keymap and this guide for some days until you are comfortable 
with the main features. 
Everything in IntelliJ IDEA is organized in a way that you, generally speaking, won't need your mouse from the moment 
you have opened your IDE. 
Therefore, the first thing I want you to do is to click on Help in the menu bar and print the *Default Keymap Reference*.
The short-cuts are similar on all systems, 
although on Mac OS X there are a few differences.
The biggest one is that the `Cmd` key is used when the other systems use `Ctrl`. 
For the guide here, I will use the shortcuts for Linux and Windows which use `Ctrl`.

## Autocompletion

Autocompletion is probably the very first feature you will notice when you start to use IDEA. It is implemented in a way that it works without the need for a special shortcut. It will silently pop-up during typing and suggest the most likely function names or variables.

You have several ways to use one of the suggestions from the autocompletion window. If you are happy with the very first one that is selected, then just press `Enter` or better, use `Ctrl`+`Shift`+`Enter`. The latter is called *Smart Enter* and does a lot of useful things in different situations. In the case of autocompleting a function name like `Plot`, it will insert braces for you and place the cursor inside. So when you type `P3` and you are happy with the `ParametricPlot3D` at the top of the suggestion list, then press `Ctrl`+`Shift`+`Enter` and you are left with `ParametricPlot3D[]` and the cursor between the braces. If the word you are completing is not a function, like `PlotRange`, which is an option, `Smart Enter` will just insert the word without braces.

Note that you can use the up- and down-arrows to start navigating in the list of completion suggestions. Usually, this is not necessary because with Camel Humps you can often specify the word uniquely. By the way, camel humps are the upper cases letters in a long function name: For instance `PP3D` for `ParametricPlot3D` or `LLICP` for `ListLineIntegralConvolutionPlot`. In fact, you don't have to specify every camel hump. You can leave some out and IDEA will happily give you correct suggestions anyway.

You can always invoke autocompletion manually (if you have e.g. pressed Esc to close the autocompletion popup) by using `Ctrl`+`Space`. If the completion window is already open, then you will see that the first entry will be highlighted: the completion is selected just like when you use the arrow keys. On such a selected entry in the completion list, you can always use open the documentation of the function using `Ctrl`+`Q`. Maybe this is important so let's make a short side-tour right here:

With `Ctrl`+`Q` you can open the documentation of the function your cursor is currently over. This works for operators too! Try to write `fun::myMsg = "Hello you"` and use the shortcut when you are next to the `=` or between `::`. The plugin comes with the documentation of all built-in functions and operators.

Back to how to use autocompletion: We have seen already that you can use `Enter` to simply insert the completion and Smart Enter (`Ctrl`+`Shift`+`Enter`) to do something more clever as it e.g. inserts braces for you. There is a third option: the `Tab` key. This is especially useful if you have a word right to your cursor and you want to replace it with the current selection. Let's say you have written `GridLinesStyle` but you made a mistake because you wanted to have `GridBoxSpacings`. Do the following, go directly between the letters `d` and `L` in `GridLinesStyle` and type `BS`. When the correct suggestion pops up, press `Tab` and see that the rest of the word is replaced.

There are two more things which are extremely helpful. The first is called *Smart Completion* and works only in specific places. You can use it when you are inside any function call like `Plot[]`. The shortcut is `Ctrl`+`Shift`+`Space` and you can use it to insert the specific options of the function you are in. This means, in the case of `Plot[]` and with the cursor inside the braces, after pressing Smart Completion all the options of `Plot[]` will pop up and you can simply insert them. It's even better, you can just start typing for instance `Plot[x,{x,0,1},PR]` and when you then press Smart Completion, it will preselect the list of options and show only the ones that match the Camel Humps. This Smart Completion will work in a similar fashion if you are inside `Message[]`, only that it will search your code for messages you have defined and show them as a suggestion.

Finally, sometimes even the clever autocompletion will not show the symbol you have defined anywhere (I want to know if something like this happens!). For those cases, there is an emergency autocompletion which can be invoked with `Ctrl`+`Alt`+`Space`. This one will show you all symbol names you have used anywhere in the file. If nothing helps, this one does.

# Moving around

During coding, nothing is more annoying than taking the hand off the keyboard to use the mouse. There are some keys you should definitely remember because they probably spare you some of those mouse events. First, holding `Ctrl` down and using left and right on the arrow keys lets you jump expression-wise. If you are inside a deeply nested construct, you can move with `Ctrl`+`[` or `Ctrl`+`]` to jump to the beginning or ending of the current scoping expression. You can use `Alt`+`Up`/`Down` to jump between expressions at file-scope, which are usually the single function definitions you made. Holding `Ctrl` down while using the arrow keys for up and down lets you scroll the document without moving the cursor position. If you want to navigate to a different file tab, you can use `Alt` and `Left`/`Right`.

Finally, with `Ctrl`+`E` you get the recent files dialog which lets you move through your current files easily. `Ctrl`+`Shift`+`E` gives you the dialog where the files are sorted by edit time. To switch to the project pane you can simply use `Alt`+`1` and note that all the other panels can be accessed in the same way using the appropriate number. If you want to move back to the editor, just press `Esc`. The *Structure View* can be accessed by using `Alt`+`7`. Very important is, when you are in the *Project View*, the Structure View or in one of the Recent Files views, you can not only move around with the arrow keys, you can just start typing to search for a name.

# Selecting Text

Selecting text works like usual by holding the `Shift` key and using the arrow keys or page-up and page-down. One incredibly useful feature is the selection of increasing/decreasing expressions which can be invoked with `Ctrl`+`W` and `Ctrl`+`Shift`+`W`. The big advantage of this type of selection is that you are often left with valid code if you cut the selection out and your braces are still balanced. Additionally, you can use `Ctrl`+`Shift`+`]` to select until the closing brace of the function you are currently in.

One very nice feature, once you have a selected code block, is the usage of `Ctrl`+`Shift`+`Up`/`Down` which will move the whole selection block through your code. This is extremely helpful if you want to re-arrange blocks of code.

# Live Templates and Surround With

*Live Templates* are very short abbreviations for a bigger code construct, for instance, `mdl` followed by a `Tab` key will insert a complete `Module[{vars}, Null]` with template positions `vars` and `Null` you can fill in. To move between the template positions, just use `Tab`. The Live Templates will appear in the autocompletion box too, together with a description of the template. In general, we have tried to stay consistent and template abbreviations are the function names without the vowels: `mdl`→`Module`, `wth`→`With`, `tbl`→`Table` etc. The complete list can be found under *Settings* → *Live Templates* → *Mathematica*. If you don't believe how useful this is, then try `usg` and start typing the function name.

Another highly used feature of mine is *Surround With* which lets you surround a select portion of text with all kinds of things. In Mathematica, you often want to surround an expression with another function. This can now be done easily: Use `Ctrl`+`W` to select the expression you want to surround and then press `Ctrl`+`Shift`+`T` and then `Enter` (or `1`). With this, it is now even very easy to turn a larger portion of code into an anonymous function.

# Structure View

The Structure View is one of the latest features. In short, it gives you a direct and clean way to see all the definitions in your file. It will extract function definitions, variable assignments, usage messages, setting of options and attributes, setting of tags and upvalues and some more. The Structure View can be turned on with `Alt`+`7` and you have several ways to adjust its behavior. First, you should use the small gear-wheel icon to turn on the Toolbar. There, you can (from left to right) sort all assignments in the structure tree by name or by line number. Furthermore, you can group the entries by the type of the assignment (`:=`, `=`, Options, Attributes, etc.) or by name. The other buttons are for expanding and collapsing the group nodes and for synchronizing the Structure View with the cursor position in the file.

In a highly complex source file, the Structure View is very helpful to find definitions. Remember that you can search all visible nodes in the Structure View simply by starting to type. Expanding the nodes can be done with `Ctrl`+`+` and collapsing with `Ctrl`+`-` which is (again) faster than taking the hand off the keyboard and using the mouse.

