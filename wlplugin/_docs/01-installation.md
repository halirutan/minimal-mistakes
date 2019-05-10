---
title: "Installing the Wolfram Language Plugin"
permalink: /docs/installation/
excerpt: "How to quickly install the Wolfram Language Plugin."
last_modified_at: 2019-02-18
toc: true
toc_sticky: true
---

The Wolfram Language Plugin works with IntelliJ IDEA and a wide range of derived products like, e.g.  CLion, PyCharm, 
RubyMin, Android Studio, WebStorm and many more.
This gives you the opportunity to develop your Wolfram Language code in the IDE that you like the most.
More importantly, however, it allows for the development of packages that use other technologies like `JLink` or 
`LibraryLink` inside an IDE which is most appropriate for Java (IDEA) or C/C++ (CLion).

## Install an IntelliJ IDE

If you start from scratch, download 
[IntelliJ IDEA here](https://www.jetbrains.com/idea/download/).
If you don’t have a licence for the Ultimate Edition, the free Community Edition is also fine.
All IntelliJ products are available for Windows, macOS, and Linux.
The Wolfram Language Plugin will work with IntelliJ version 2018.3 or newer.

## Install the Wolfram Language Plugin

Once you started your IntelliJ IDE, you will see the initial Welcome screen.

[![Image](/assets/images/doc/IDEAStartScreen.png)](/assets/images/doc/IDEAStartScreen.png)

Click on **Configure | Plugins**, search for "Wolfram Language" in the Marketplace tab (IntelliJ 2019 or later) or use
**Browse repositories** (IntelliJ 2018).
If you’ve been using IntelliJ previously, then open the plugins window from **File | Settings | Plugins**.

Install the Wolfram Language Plugin and restart IntelliJ IDEA to finish the installation.

The Wolfram Language Plugin updates automatically to the latest version once it is available on the
[Jetbrains Plugin Repository](https://plugins.jetbrains.com/plugin/7232).
Newer version of the plugin might require an up-to-date IntelliJ IDE and, therefore, it is advised to use the latest
version of IntelliJ IDEA.
Once a new version of the plugin is available, the IDE shows a notification.

## Upgrading from version 2.4.4 to version 2019

Between version 2.4.4 and version 2019 of the Wolfram Language Plugin many of the core algorithms and data-structures
were rewritten.
As a consequence, the internal representation of caches and indexes have changed and you might experience odd behavior.
Please clear and rebuild the caches by clicking **File | Invalidate Caches/Restart** which will restart IDEA and rebuild
all structures.

## Using EAP (beta) releases

Testing new features or working on larger changes requires testing-phase to ensure the plugin works correctly and there
are no regressions. To install beta-releases, you need to add the *beta repository* to your IntelliJ IDEA settings. 
After that, you will get update-notifications each time a new beta version is available which is far more frequently 
than updates for stable versions.

To add the beta channel in IDEA 2018.3 or later, go to **File | Settings | Plugins**. In this setting page, click on 
the ⚙ icon in the upper right corner:

[![settings](/assets/images/pluginDialog.png)](/assets/images/pluginDialog.png)

Choose **Manage Plugin Repository...** from the popup and in the appearing dialog, add the URL 

```
https://plugins.jetbrains.com/plugins/beta/list
```

as shown here:

[![settings](/assets/images/pluginRepository.png)](/assets/images/pluginRepository.png)

I a development version of the plugin is available, you can now install it by 
After closing this window, you can install the beta-version for "Wolfram Language" in the *Browse 
Repositories* window and you will find that the beta version is displayed and ready for install.

## Downgrading

Especially in beta releases, you might experience bugs which affect your work.
However, you can always downgrade to a previous version that worked for you.
Go to the [Wolfram Language Plugin](https://plugins.jetbrains.com/plugin/7232)
repository page, and there you can download previous versions.
Make sure you download the plugin version which is compatible with the IntelliJ version you are using.
If you’d like to downgrade to a previous beta version you’ll need to click the `beta` button in the **Download 
plugin** section.
Once you’ve downloaded the version you want, install it using **Settings | Plugins | ⚙ | Install from disk...**