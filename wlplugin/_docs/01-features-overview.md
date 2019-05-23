---
title: "Feature Overview"
permalink: /docs/feature-overview/
excerpt: "Currently under construction"
toc: false
---

The following is a list of features provided by the Wolfram Language Plugin.
Note that this is only a small fraction and the vast majority of features comes from IntelliJ IDEA itself that gives you
an excellent environment to manage files, have a project view, share and manage code through version control systems like git,
and provides excellent editing.

## Code Highlighting and formatting

* Context-aware syntax highlighting of _Mathematica_ code. The plugin deduces if a symbol (variable, function) is globally defined or if it is bound in a smaller context like `Module`-variables.
* Highlighting of pattern variables in function definitions or replacements using `RuleDelayed` (`:>`).
* Highlighting of anonymous functions, e.g. `#+3&`.
* Highlighting of special constructs like `fun::usage`, comment annotations like `(* ::Section:: *)` or (* :Author: Brian Briggs *).
* Highlighting of matching braces and the display of the current context on the left
* Automatic formatting and indentation of code.

## Code Completion

For details, please see the [Code Completion section](/docs/03-code-completion.md).

* Autocompletion for all built-in functions.
* Autocompletion for localized variables inside `Module`, `Block`, `Table`, `Compile`, and other constructs like plotting commands.
* Template completion for common code constructs. Write e.g. `mdl` and press `Tab` to get a `Module[{..},..]`. For a complete list look at this [xml file](https://github.com/halirutan/Mathematica-IntelliJ-Plugin/blob/develop/resources/de/halirutan/mathematica/codeinsight/livetemplates/mathematica.xml).
* Smart completion for options of a function.
* Smart completion to insert defined messages in `Message[..]`.
* Smart completion for special comment annotations.

## Advanced Editing

* Renaming of local variables bound to any of functions that localize their variables. This includes `Module`, `Block`, and much more.
* Renaming of global symbol definitions including their usages in the `::usage` message string.
* Surround code with other code. This lets you quickly surround an expression with braces, functions, anonymous function, or any of the live temples like `Module`.
* Smart Enter to auto-insert brackets or a template for functions during autocompletion.
* Expand selection by expression. This lets you quickly expand (shrink) a selection by including surrounding expressions.
* Comment/uncomment region or line.
* Smart insertion/deletion of braces and quotes.
* Support for named characters like `\[Gamma]` that can be folded to their real UTF-8 character

## Error Annotations

Error annotations help you to find suspicious code parts that might be an error quickly.

* Version annotator. Select a Mathematica version you are developing for and all functions that are only available in a later version will be marked as an error.
* Highlighting of `(* TODO: ... *)` comments which additionally appear in the todo tool window
* Missing comma error highlighting.
* Missing semicolon in compound expressions.
* Spellcheck for your code, strings, and comments.

## Navigation

* Goto definition will jump to the first place where a symbol is assigned a value
* Goto related symbol will show all usages of a function or symbol and lets you quickly navigate through long code files.  
* Structure View for your package file showing a detailed list of defined functions, messages, and much more. You can quickly navigate from the structure view to the code.
* Code folding. Fold expressions, function definitions or even whole sections as defined by comments like `(* ::Section:: *)` to hide code
* Documentation lookup for all built-in functions.

## Creation of Template Code

* Creation of complete _Mathematica_ projects with boilerplate code
* Creation of package files with template code




