---
title: "Fenced code blocks in markdown"
permalink: /docs/markdown-support/
toc: false
---

The Wolfram Language Plugin also works with JetBrains' Markdown Support plugin which can be installed when you need
to work with markdown files.
It provides highlighting for the code in the text-editor and many static website generators take the language
tags after the initial triple-ticks into account and highlight code accordingly.

The following Wolfram Language tags are currently supported: `mathematica`, `wl`, `mma`, and identifiers which 
contain `wolfram`

[![Markdown Highlighting](/assets/images/doc/05-markdown-support.png){: .align-center}](/assets/images/doc/05-markdown-support
.png)

Note that code snippets in markdown are often incomplete and might contain warnings regarding unresolved symbols.
Each snippet stands on its own and cannot use other code blocks for resolving symbols. Additionally, automatic
indentation does not work for fenced code blocks.
{: .notice--info}