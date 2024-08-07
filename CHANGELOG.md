# Extra Tools Pack Change Log

## 2024.7.1 (2024/07/29)
* integrates the latest version of Extra Icons (2024.6.4, 2024/07/29):
  * implement [#184](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/discussions/184):  support `.gitea` folders and `*.yml` files in `workflows` subdirectories.
  * fix [#183](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/183): custom icons should apply to files and folders only, not to class members like properties, methods and nested classes.
  * fix [#185](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/185): `requirements.txt` should have a custom icon in PyCharm.
  * add more alternative icons for Java Records.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.3.1, 2024/07/29):
  * [request #1](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/1): add colors to the NuGet icon.
  * fix [#3](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/3): the Project icon should be yellow, even when inactive (new UI, dark theme).

## 2024.6.1 (2024/07/21)
* integrates the latest version of Extra IDE Tweaks (2024.12.1, 2024/07/21):
  * the **Open Editors** tool window is now using [JetBrains' Tree](https://plugins.jetbrains.com/docs/intellij/lists-and-trees.html#jblist-and-tree) implementation instead of JTree, leading to some benefits like a better UI. Drawing a tooltip with complete text of an item if the item doesn't fit into the list box width. It also integrates the **Speed Search** functionality, [similar to Speed Search for Tool Windows](https://www.jetbrains.com/help/idea/speed-search-in-the-tool-windows.html): type text when the Open Editors tool window has focus, and the selection moves to the first item that matches the specified string.
  * fix `Slow operations are prohibited on EDT` issues when using the Open Editors tool window in an EAP IDE.
  * minor performance improvements.
  * fix a license detection [issue](https://github.com/jonathanlermitage/ij-extra-all-plugins-pack-pub/issues/1).
* integrates the latest version of Extra Icons (2024.6.3, 2024/07/21):
  * UI improvement (for non-EAP IDEs only): use IDE's file chooser dialog instead of the regular Swing file chooser dialog.
  * minor performance improvements.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.2.1, 2024/07/21):
  * add colors to the Server icon.

## 2024.5.1 (2024/07/08)
* Extra Tools Pack now integrates all Extra ToolWindow Colorful Icons free and paid features. **If the Extra ToolWindow Colorful Icons plugin is installed in your IDE, please uninstall it, restart your IDE, and keep using Extra Tools Pack.**
* integrates the latest version of Extra IDE Tweaks (2024.11.1, 2024/07/08):
  * make the `File > Favorite Projects` and `File > Trusted Locations` menus available during indexing.
  * Favorite Projects: add a menu item to re-open favorite projects while preserving their order of registration. Useful if you're in the habit of opening several projects systematically in the same order.
  * improve Tool Windows Label Override: reapply user's rules if the IDE has reverted to a tool window label (it can happen when enabling AI Assistant).
  * minor performance improvements and enable future performance improvements for 2024+ IDEs (based on JBR21).
  * general stability improvements. Some internal concurrent components were not ideally synchronized, which could lead to minor performance degradations. This is now fixed.
* integrates the latest version of Extra Icons (2024.6.2, 2024/07/08):
  * minor performance improvements and enable future performance improvements for 2024+ IDEs (based on JBR21).
  * general stability improvements. Some internal concurrent components were not ideally synchronized, which could lead to minor performance degradations. This is now fixed.
  * support [Vale](https://vale.sh) `.vale.ini` files.

## 2024.4.1 (2024/06/26)
* integrates the latest version of Extra IDE Tweaks (2024.10.1, 2024/06/26):
  * feature: **Favorite Projects**. Go to settings and add projects to favorites, organize them with groups, and gain fast access to your favorite projects via `File > Favorite Projects`.
  * settings: table lines can now be reordered.
  * settings: fix NPE when adding empty lines in tables.
  * `File > Trusted Locations`: visual and performance improvements.
* integrates the latest version of Extra Icons (2024.6.1, 2024/06/26):
  * partially implement [IDEA-352785](https://youtrack.jetbrains.com/issue/IDEA-352785): provide icons for Kotlin classes, interfaces, enums, etc., without the small "K" badge.

## 2024.3.2 (2024/06/21)
* 2024.2 IDEs now bundle the Chinese Language Pack plugin. For these IDEs, plugin's Chinese UI is now applied only if you select the Chinese locale (File > Appearance & Behavior > System Settings > Language and Region). For older IDEs, plugin's Chinese UI is applied if you download and enable the Chinese Language Pack plugin.
* integrates the latest version of Extra IDE Tweaks (2024.9.2, 2024/06/21):
  * minor code and UI rework.

## 2024.3.1 (2024/06/15)
* replace the plugin's custom error reporter by the new IDE [Exception Analyzer](https://plugins.jetbrains.com/docs/marketplace/exception-analyzer.html). This is an easy way to report plugin exceptions from IntelliJ Platform-based products to plugin developers right on JetBrains Marketplace, instead of opening an issue on the plugin's GitHub repository.
* integrates the latest version of Extra IDE Tweaks (2024.9.1, 2024/06/15):
  * schedule GC on local JVMs: kill `jcmd` processes spawned by plugin if they are not responding. This can happen when `jcmd` processes are executed when your computer wakes up from sleep/hibernation.

## 2024.2.1 (2024/06/10)
* fix plugin error reporter's configuration. It was asking users to open issues on the Extra Icons GitHub repository instead of the Extra Tools Pack one.
* integrates the latest version of Extra IDE Tweaks (2024.8.7, 2024/06/10):
  * `File > Trusted Locations` can now also display projects in first-level subdirectories. Disabled by default, you can enable this in settings.
  * improve the performance of `File > Trusted Locations` and run it in a background task. The list of projects found is computed at IDE start then it's cached until next IDE start, or if you refresh it by going to `File > Trusted Locations > Refresh from Disk`.
  * minor code and UI rework.

## 2024.1.4 (2024/06/03)
* the first public release, based on the latest versions of Extra Icons (2024.4.2, 2024/05/24) and Extra IDE Tweaks (2024.8.6, 2024/06/03).
