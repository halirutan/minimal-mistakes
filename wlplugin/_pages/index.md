---
title: "Wolfram Language Plugin 2019 for IntelliJ platform based IDE's"
layout: splash
permalink: /
header:
  overlay_image: /assets/images/wlSplash.jpg
  actions:
    - label: "<i class='fas fa-download'></i> Download Beta Version"
      url: "/docs/installation/#upgrading-from-version-244-to-version-2019"
excerpt: "Turn your IntelliJ IDE into a powerful development tool<br /> for working with Wolfram Language packages.<br />"
---

This website for the new Wolfram Language IntelliJ Plugin is currently under construction. Many details, especially in 
the documentation, are still missing and will be added in the future. Likewise, the new plugin 
version
2019 is currently only available as beta version. Please refer to the 
[documentation](/docs/installation#upgrading-from-version-244-to-version-2019) if you 
want to try it.
{: .notice--info}

## What is the Wolfram Language Plugin?

The Wolfram Language Plugin is an easy-to-install plugin for IntelliJ platform based IDEs which turns them into a powerful development tool for the Wolfram Language and Mathematica code.
The plugin is designed for package developers who prefer superior editing features, advanced code insight, and an intelligent IDE over a notebook-based approach.
It integrates seamlessly into the full-fledged IntelliJ platform with project management, version control, and its exceptional code editor.

The strength of the plugin is that it analyses your code on-the-fly which allows for intelligent auto-completion not only for
all functions built into the Wolfram Language, but also for local variables, package functions and even symbols from external packages.
You can navigate directly from the usage of your function to its implementation or vice versa.
The Structure View provides a unique way to inspect all package functions and makes navigation to usage messages, attributes, options,
or definitions painless.
Many advanced features like live templates, smart completion, refactoring, intentions, annotations, and code-folding help you to write correct code at an incredible speed.
In combination with the features of IntelliJ IDEA, it gives you a development experience you never want to miss again.

## Feature Highlights


![img](assets/images/Completion.png){: .align-center}

### Code Completion

Code completion is available for all built-in functions and symbols available in the Wolfram Language.
Since the language uses camel case consistently for all symbols, the auto-completion will understand when you shorten
long function names like `GaussianOrthogonalMatrixDistribution` with `GOM` and provides you with correct suggestions.
All variables scoped by `Module`, `Block`, `With`, but also by other constructs like `Table`, `Compile`, etc. can be auto-completed,
as well as all functions defined in your project.
The plugin is aware of options for all Wolfram Language functions and provides you with correct completion candidates.
This _smart completion_ also works on other places and helps to, e.g. insert defined error messages when using `Message[..]`.
[More about Code Completion...](/docs/code-completion/)


![img](assets/images/LiveTemplates.png){: .align-center}

### Live Templates and surrounding code

Live Templates provide expandable boiler-plate code for most common Wolfram Language constructs. Things like `Module`,
`Table` or `Function` definitions can directly be inserted and filled with content.
These templates also work when wrapping them around existing code or selected text.
In the screen-shot above, the initial `Table` is inserted by expanding the short `tbl` with the `Tab` key.
A simple short-cut is invoked to wrap everything in a `Module`.
Surrounding existing expressions additionally works with arbitrary functions and parentheses.
[Learn more about Live Templates...](/docs/live-templates/)


![img](assets/images/Rename.png){: .align-center}

### Refactoring

Renaming functions and symbols with all their usages is often enough one source of bugs.
The Wolfram Language Plugin makes this painless by allowing for renaming of local variables, arguments and 
functions.
The screen-shot above shows how easy it is to rename all appearing symbols in the example.
[More about Refactoring...](/docs/refactoring/)

![img](assets/images/StructureView.png){: .align-center}

### Code Navigation

Besides the many features for navigating the code, finding symbols or jump to certain definitions, the Structure View
provides a compact outline of a Wolfram package.
It differentiates between function definitions, options, attributes, etc. and allows for a direct navigation to the
appropriate location inside the source code.
The display can be sorted by symbol names or types of definition and makes navigation inside package code easy.
[More about the Structure View...](/docs/structure-view/)
