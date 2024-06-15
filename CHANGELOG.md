# Extra Tools Pack Change Log

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
* first public release, based on latest versions of Extra Icons (2024.4.2, 2024/05/24) and Extra IDE Tweaks (2024.8.6, 2024/06/03).
