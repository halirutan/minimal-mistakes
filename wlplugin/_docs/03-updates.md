---
title: "Updating and Beta-Releases"
permalink: /docs/updates/
excerpt: "How to update the Wolfram Language Plugin to the latest version."
toc: true
toc_sticky: true
---

The Wolfram Language Plugin updates automatically to the latest version once it is available on the
[Jetbrains Plugin Repository](https://plugins.jetbrains.com/plugin/7232).
Newer version of the plugin might require an up-to-date IntelliJ IDE and, therefore, it is advised to use the latest
version of IntelliJ IDEA.
Once a new version of the plugin is available, the IDE shows a notification.

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