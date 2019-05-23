---
permalink: /about/
title: "About the Wolfram Language Plugin"
toc: false
author_profile: true
---

The work on the Wolfram Language Plugin started in late 2012 as a proof-of-concept and was planned as a community 
project to provide an alternative to the Wolfram Workbench.
The reasons for starting the development were twofold: As a long-time user of IntelliJ IDEA 
I wanted to use the Wolfram Language within IDEA and its incredible editing features. Additionally,
I never really got to like Eclipse which is the underlying IDE of the Wolfram Workbench.

When starting to work on the plugin, the toughest parts were to get used to the large IntelliJ SDK and to 
implement a parser for Wolfram Language which is both error-tolerant and reasonably fast.
It must be fast, because on each keystroke the whole file is reparsed and the resulting abstract syntax tree is
used to determine syntax highlighting, resolve where your functions are defined, and provide advanced code insight
features. The parser must be error-tolerant because most of the time while you're writing, your code is incomplete
and syntactically wrong.
The parser must account for that and process the whole file, even if it contains errors.
One further complication is that the syntax of the Wolfram Language, although very well documented, has no official
specification and there are some quirks in the language that pop up from time to time.
To give an example, try to guess the result of `{1,2,3}/.1->4` without evaluating it.

In 2016, the plugin was established very well and version 2.4.4 from 2017 has currently over 15.000 unique downloads.
Still, some design choices of the plugin's internal data structures made it hard to further employ the capabilities
of the IntelliJ platform easily.
The only option to not turn implementing further features into a chaotic mess was to rewrite some of these core
algorithms.
I started to work on this in 2017 and since then features like code completion across files, refactoring, code 
inspections and adding other packages as "libraries" were improved or added.
Although these features were available as a beta, the 2019 version of the Wolfram Language Plugin is the first 
release which contains all these new capabilities.

During the years of development, I was furtunate to receive a lot of support from people who encouraged me to improve
the plugin and implement more features.
To be able to rely on expert users who report bugs and discuss features is a blessing and I thank all these people
for their continuous support.

The work on the Wolfram Language Plugin happens during my free-time or on weekends.
It does not only consist of writing code.
A large portion is reading IntelliJ IDEA's sources to understand how things are implemented and dig into the details
of the Wolfram Language.
Other things include creating icons, write documentation and actually using the plugin in my projects.