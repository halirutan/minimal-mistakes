---
title: "Frequently Asked Questions"
permalink: /docs/faq/
excerpt: "Frequently asked questions about the Wolfram Language Plugin."
toc: false
---

### Is there a plan for the development?
 
Yes. For version 2019, a large part of the code-base was rewritten to allow for more sophisticated code-insight
like package-wide completion and navigation.
A good part of the development time is spent on implementing new features and fixing bugs.
The goal for the near future is to provide a better support for Paclet-based packages.
However, often the direction of development is influenced by users with good arguments for a specific feature.
If you are interested in discussions, please visit the 
[Gitter chat](https://gitter.im/Mathematica-IntelliJ/Lobby) and report bugs as  
[GitHub issue](https://github.com/halirutan/Mathematica-IntelliJ-Plugin/issues).

### Can I deploy my package?

Basically yes. Deploying an old-style package is not more than creating a `.zip` file from your package sources that 
users can extract into their `Applications` directory. You can easily create an *Artifact* in IDEA that does this. 
For Paclet-based packages, the best way to deploy code is to run `PackPaclet` on the directory which contains the 
`PacletInfo.m` file.

### Can I run or debug my code inside IntelliJ IDEA or build documentation?

Currently not. Both actions require a Mathematica kernel and while the communication with the kernel is well-documented,
the way the Wolfram Workbench interacts with the Mathematica front-end is not.
That means, information about debugging code or building documentation are scarce and hidden in the implementation of
Wolfram Workbench.
Especially building package documentation has proven to be extremely fragile and does not work well when supporting
several Mathematica versions.
Hopes are that in the distant future Wolfram will provide an official and stable way how this is done so that it 
can be implemented for the Wolfram Language Plugin as well.

