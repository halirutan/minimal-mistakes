---
title: "Inspections, Intentions and QuickFixes"
permalink: /docs/inspections-quickfixes/
excerpt: "Currently under construction"
toc: false
---

[Code Inspections inside IntelliJ IDEA](https://www.jetbrains.com/help/idea/code-inspection.html) are used to highlight 
probable errors by analyzing the structure and content of your code.
They run in the background automatically and issue warnings that help you to write correct Wolfram Language code.
Each inspection has a definite purpose and can be adjusted or turned off easily.
You can find the settings for all Wolfram Language inspections by navigating to 

- **File | Settings | Editor | Inspections | Wolfram Language**

The listing there shows all available inspections and contains clear descriptions how they work.
Below you find a more detailed description of two specific inspections that gives you more insight how they work.

## Language Version Inspection

If you develop Wolfram packages, you might not have the latest version available or, which is more likely, you try
to keep some backward compatibility with former versions of the Wolfram Language.
This inspections will help you by flagging functions and constructs that are not yet available in 
the Wolfram Language version you are developing for. 

Below, you see a screenshot of a file that contains an `Association` and functions that are not available in *Mathematica* version 9. The inspection will mark them as errors and give you helpful insight in which version the feature was introduced to *Mathematica*

[![Language Inspection][1]{: .align-center}][1]

There are two ways to select the version you are developing for and both can be set in the settings page

- You can use the version of your *Mathematica* installation that you can set by creating a new or selecting a *Mathematica SDK* under *File  → Project Structure → Project → Project SDK*. In this case, select checkbox *Use Project SDK Language Level* as shown in the image below.
- You can ignore your Project SDK and set a *Mathematica* version explicitly by unchecking *Use Project SDK* and by selecting a version.

## Missing comma or semicolon

Missing commas can lead to very surprising behavior because *Mathematica* treats expressions that are separated by whitespace as multiplication. In long expressions that are broken into several lines, this can be a hard to spot an error. Consider the following code

{% highlight wl %}
{% raw %}
Join[
 {1, 2, 3, 4, 5, 6, 7}
 {1, 2, 3, 4, 5, 6, 7}
 ]
{% endraw %}
{% endhighlight %}

This is completely correct code but it leads to the result `{1, 4, 9, 16, 25, 36, 49}` which is clearly not intended here. The reason is that the line break with the missing comma is interpreted as multiplication of the two lists. Now consider that for instance in a `Module` with a very long list of variables this leads to hard to find bugs. IDEA will help you out by annotating such places

[![Missing comma inspection][2]{: .align-center}][2]



The same issue can happen with missing semicolons resulting in unwanted multiplication of expressions. IDEA will warn you about those issues as well. Note that the small indicators on the right side where the scrollbar is point to places where errors and possible bugs were found

Finally, in package code some user prefer to make a semicolon after each definition others don't. Most of the users although will mix both styles together. IDEA has a separate inspection that indicates missing semicolons at file scope that helps you to put semicolons consistently if you prefer that.


[1]: /assets/images/doc/03-language-version-inspection.png
[2]: /assets/images/doc/03-missing-comma.png
