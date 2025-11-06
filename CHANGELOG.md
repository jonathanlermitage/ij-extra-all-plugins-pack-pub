# Extra Tools Pack Change Log

## 2025.1.19 (WIP)
* integrates the latest version of Extra Icons (2025.1.17):
  * implement [#223](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/223): support SQL Script files. 2025.3 EAP IDEs introduce a new icon for (some?) SQL files, but it looks like the icon for generic Script files. A new icon association has therefore been added in Extra Icons to restore the previous SQL icon (see "SQL Script" in the  Plugin icons list, New UI only).
  * implement [#224](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/224): support Rebar3 `rebar.config` and `rebar.lock` files.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.16):
  * add colors to the Apply Changes and Restart Activity run configuration icon (Android Studio, New UI).
  * add colors to the Apply Code Changes run configuration icon (Android Studio, New UI).
  * add colors to the Assemble app run configuration icon (Android Studio, New UI).
  * add colors to the Attach Debugger to Android Process run configuration icon (Android Studio, New UI).
  * add colors to the Sync Project with Gradle Files run configuration icon (Android Studio, New UI).
  * add colors to the App Links Assistant tool window icon (Android Studio).
* integrates the latest version of Extra IDE Tweaks (2025.1.15):
  * **highly recommended update**: prevent a potential IDE freeze when the `Always Excluded Folders` feature is enabled and the IDE is opening a very large project or many smaller projects that need a complete re-indexing, and too many modules are present. This is an improvement of the original fix provided in the 2025.1.12 (2025/08/27) plugin release. The `Always Excluded Folders` was disabled for projects with more than 20 modules, but the IDE may also invoke this function by passing the modules one by one. Per example, with a project with 1600 modules (like the IntelliJ Community sources), it invoked the function with the 1600 modules, so I blocked it, but just after that, it also invoked the function 1600 times, one time for each module, which may freeze the IDE for a long time. This is now fixed by caching (in memory) the number of modules for the opened project.

## 2025.1.18 (2025/10/16)
* fix usage of some JetBrains deprecated APIs, improving the compatibility with future IDEs (2025.3+).

## 2025.1.17 (2025/10/08)
* fix usage of some JetBrains deprecated APIs, improving the compatibility with future IDEs (2025.3+).
* integrates the latest version of Extra Icons (2025.1.15):
  * user icons: you can now choose to check file paths against the original paths or lowercase paths. [Documentation](https://jonathanlermitage.github.io/ij-extra-tools-pack-docs/extra-icons-user-icons.html#conditions).
  * update the JUnit icon: it now uses the JUnit 6 logo. You can still use the JUnit 5 icon if you want (see JUnit alternative icons).
  * add a new Deno icon. The old Deno icon is still available as an alternative icon.

## 2025.1.16 (2025/09/15)
* integrates the latest version of Extra Icons (2025.1.14):
  * support more files when choosing the `Always prefer old UI icons` option in Extra Icons' advanced settings. This is an effort to make this mode more consistent for people who prefer the classic icons (even when using the New UI), or people who are not comfortable with the wireframe icons that come with the New UI.
  * fix [#214](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/214): support Razor `*.razor` and `.cshtml` files.
  * rework the dark icon variant of Contact files.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.14):
  * fix support of the Feature Trainer tool window icon. JetBrains changed the path of this icon in recent IDEs, so I needed to adapt my code.
  * add colors to the Compare Versions tool window (New UI only, the Classic UI tool window has no icon, so I can't change it for now, but I'm working on a workaround).

## 2025.1.15 (2025/08/27)
* integrates the latest version of Extra Icons (2025.1.13):
  * support Firefox extension files `*.xpi`.
  * support [Forgejo](https://forgejo.org) `.forgejo` folders.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.13):
  * rework and add colors to various Rider and GoDot toolbar and tool window icons: dotCover, dotMemory, dotTrace, Assembly Explorer, Monitoring, IL, DPA, Build whole solution, Syntax Tree Visualizer / Roslyn analyzers, .NET Project Run / Debug Configurations, various other .NET Run / Debug Configurations, GoDot Scene Preview, GoDot Script, dotcover Success status, dotcover Ongoing Success status, Tests toolwindow.
  * add colors to the [AI Playground](https://plugins.jetbrains.com/plugin/27370-ai-playground) tool window icon. This also fixes the icon size when using the Classic UI.
* integrates the latest version of Extra IDE Tweaks (2025.1.12):
  * prevent a potential IDE freeze when the `Always Excluded Folders` feature is enabled and the IDE is opening a very large project or many smaller projects that need a complete re-indexing.

## 2025.1.14 (2025/08/05)
* integrates the latest version of Extra Icons (2025.1.12), Extra ToolWindow Colorful Icons (2025.1.12), and Extra IDE Tweaks (2025.1.11):
  * new series of workarounds for the [IDEA-376370](https://youtrack.jetbrains.com/issue/IDEA-376370/) issue. Up-voting this issue would greatly help.

## 2025.1.13 (2025/07/30)
* integrates the latest version of Extra Icons (2025.1.11):
  * workaround for the [IDEA-376370](https://youtrack.jetbrains.com/issue/IDEA-376370/) issue.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.11):
  * workaround for the [IDEA-376370](https://youtrack.jetbrains.com/issue/IDEA-376370/) issue.
* integrates the latest version of Extra IDE Tweaks (2025.1.10):
  * workaround for the [IDEA-376370](https://youtrack.jetbrains.com/issue/IDEA-376370/) issue.

## 2025.1.12 (2025/07/24)
* integrates the latest version of Extra Icons (2025.1.10):
  * better fix for [#219](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/219): the previous fix broke some icon customizations, like Docker, Helm, or Git submodules support.

## 2025.1.11 (2025/07/17)
* integrates the latest version of Extra Icons (2025.1.9):
  * fix [#219](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/219): `java.lang.IllegalStateException: WriteIntentReadAction can not be called from ReadAction` errors could occur on project loading or when refreshing icons when using 2025.1.3 IDEs or the latest IntelliJ 2025.2 EAP build (IU-252.23591.19).

## 2025.1.10 (2025/07/11)
* integrates the latest version of Extra Icons (2025.1.8):
  * reintroduce the alt icon for PHP Composer files. It had been removed by mistake.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.10):
  * new fix for [#16](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/16): `SettingsService is in unnamed module of loader com.intellij.ide.plugins.cl.PluginClassLoader` errors. 
* integrates the latest version of Extra IDE Tweaks (2025.1.9):
  * new fix for `SettingsService is in unnamed module of loader com.intellij.ide.plugins.cl.PluginClassLoader` errors.

## 2025.1.9 (2025/07/01)
* integrates the latest version of Extra IDE Tweaks (2025.1.8):
  * fix the **purge IDE's plugin download cache** feature. Archive files for installed plugins no longer required by the IDE were not deleted.

## 2025.1.8 (2025/06/27)
* integrates the latest version of Extra Icons (2025.1.7):
  * fix [#215](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/215): `com.intellij.diagnostic.PluginException: / by zero` errors.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.9):
  * fix [#16](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/16): `SettingsServiceB is in unnamed module of loader com.intellij.ide.plugins.cl.PluginClassLoader` errors.
  * add colors to the Android Profiler tool window icon.
  * rework the Android Build Variants tool window icon (New UI).
* integrates the latest version of Extra IDE Tweaks (2025.1.7):
  * fix potential `SettingsServiceB is in unnamed module of loader com.intellij.ide.plugins.cl.PluginClassLoader` errors.
  * improve the **purge IDE's plugin download cache** feature. Pending plugin installs and updates are no longer affected.

## 2025.1.7 (2025/06/13)
* the minimal IDE version is now 2024.3 instead of 2023.3.1. This was needed to use newer JetBrains APIs and stay compatible with future IDEs (2025.2+).
* integrates the latest version of Extra Icons (2025.1.6):
  * fix usage of some JetBrains deprecated APIs, improving the compatibility with future IDEs (2025.2+).
  * implement [#207](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/207): regular expressions shouldn't need to fully match. An option has been added to model conditions, which lets you choose whether a regular expression should match the entire file path or only part of a file path. The default setting is set to match the entire file path.
  * [#206](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/206): support Visual Studio `*.csproj`, `*.sln` and `*.slnx` files.
  * [#212](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/212): support Fish Shell `*.fish` files.
  * fix [#209](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/209): rework how user icon conditions are evaluated. This now respects the [documentation](https://jonathanlermitage.github.io/ij-extra-tools-pack-docs/extra-icons-user-icons.html#conditions).
  * minor visual improvements in settings dialogs.
  * general performance improvement. Performance was already good, and a new caching mechanism makes the file-icon association ~2x faster, with a minimal memory footprint.
  * rework several bundled file-icon associations.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.8):
  * fix usage of some JetBrains deprecated APIs, improving the compatibility with future IDEs (2025.2+).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): rework and add colors to the Hierarchy tool window icon.
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the Open Project main menu icon (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the JetClient tool window icons (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the SonarQube tool window icons (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the TeamCity tool window icons (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the YouTrack tool window icons (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the Search Everywhere main toolbar icon (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the IDE Settings icons (New UI).
  * [#13](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/13): add colors to the Code With Me main toolbar icon (New UI).
  * [#14](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/14): add colors to the AI Assistant main toolbar icon (New UI).
  * add colors to the Kubernetes tool window icon.
  * add colors to the UI Theme Color Picker tool window icon (appeared with 2025.2 IDEs, internal mode).
  * rework the Python Console tool window icon and add alternative icons.
  * rework the Python Packages tool window icon and add alternative icons.
  * optimize the plugin size on disk by reorganizing resource files.
  * minor visual improvements in settings dialogs.
* integrates the latest version of Extra IDE Tweaks (2025.1.6):
  * fix usage of some JetBrains deprecated APIs, improving the compatibility with future IDEs (2025.2+).
  * the **Commit Alert** feature now ignores some common files like media files (pictures and videos, PDF files, Office files, etc.), archives, and binary files. This will greatly improve the performance when committing these files. A future update will let you configure this.

## 2025.1.6 (2025/05/06)
* integrates the latest version of Extra Icons (2025.1.5):
  * additional fix for [#200](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/200): error `Class initialization must not depend on services. Consider using instance of the service on-demand instead` may occur on IDE start with IntelliJ 2025.1.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.7):
  * fix for error `Class initialization must not depend on services. Consider using instance of the service on-demand instead`.
  * various minor code reworks.
* integrates the latest version of Extra IDE Tweaks (2025.1.5):
  * fix for error `Class initialization must not depend on services. Consider using instance of the service on-demand instead`.

## 2025.1.5 (2025/04/14)
* integrates the latest version of Extra Icons (2025.1.4):
  * fix [#193](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/193): support NestJS `*.resolver.(js|ts)` files.
  * minor code reworks.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.6):
  * implement [#12](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/12): add colors to some tool window icons in various plugins for Microsoft Azure.
  * rework the Make tool window icon (New UI).
  * improve support of third-party plugins.
* integrates the latest version of Extra IDE Tweaks (2025.1.4):
  * UI fixes in the plugin's settings panel.

## 2025.1.4 (2025/03/17)
* settings can now be loaded and saved by the **Backup and Sync** plugin.
* integrates the latest version of Extra Icons (2025.1.3):
  * fix [#200](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/200): error `Class initialization must not depend on services. Consider using instance of the service on-demand instead` may occur on IDE start with IntelliJ 2025.1 EAP (251.22821.72).
  * implement [#202](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/202): support `xunit.runner.json` files.
  * implement [#203](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/203): support `log4net.config` files.
  * implement [#204](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/204): support Stryker Mutator `stryker-config.json` and `stryker-config.yaml` files.
  * support `.sdkmanrc` files.
  * settings UI: improve the User Icons table. If no user icon has yet been registered, display a message in the center of the table and a convenient way to add a first icon. Similar thing for the New Icon dialog, when no Condition has yet been registered.
  * various code reworks.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.5):
  * implement [#10](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/10): add colors to the GitHub Copilot tool window and status bar icons (welcome, Copilot, chat, connection status).
  * rework the Notifications tool window icon. The purple icon turned orange when selected.
  * add some alternative icons for the Notifications tool window icon.
  * add an alternative icon for the Structure tool window icon (the new icon introduced by IntelliJ 2025.1).
  * add colors to the Power Save Mode icons (status bar and inspection).
  * add colors to the (Android Studio) Device Explorer, Device Manager, and App Quality Insights tool window icons.
  * add colors to the (Android Studio, Gemini) AI Code Completion status icon.
  * add colors to the JetBrains Junie tool window icon.
  * important code rework: better support of icon override for the icons coming from third-party plugins.
  * improve the Chinese localization.
  * various code reworks.
* integrates the latest version of Extra IDE Tweaks (2025.1.3):
  * prevent a `Slow operations are prohibited on EDT` warning on project loading with IntelliJ 2025.1 EAP when the `Always Excluded Folders` feature is enabled.
  * various code reworks.

## 2025.1.3 (2025/02/25)
* improve the plugin's compatibility range. The minimal IDE version is now 2023.3.1 instead of 2024.1.
* integrates the latest version of Extra Icons (2025.1.2):
  * fix [#195](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/195): some custom icons are not working in Explorer in Rider.
  * fix [#196](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/196): using Presentation Mode does not resize user icons properly.
  * the zoom level set in the IDE's accessibility options is now applied to user icons. This will fix potential bad rendering (wrong scale) of user icons when using any zoom level.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.4):
  * implement [#8](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/8): add colors to the Notifications tool window icon.
  * implement [#9](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/9): add colors to the Coverage tool window icon.
  * settings UI: add a search field to filter the icon table. This should help you find icons to (de)activate.
  * improve the way IDE icons are replaced by custom icons, especially when using the New UI and deactivating the Compact Mode.

## 2025.1.2 (2025/01/27)
* update the plugin compatibility list: avoid collision with the new Extra ToolWindow Colorful Icons Lifetime plugin.

## 2025.1.1 (2025/01/21)
* integrates the latest version of Extra Icons (2025.1.1):
  * you can now add icons to Actions in menus. For example, add an icon to the `right-click > Git > Rebase...` action. You can also overwrite an action's icon if it already has one. For icons associated with intermediate menus, JetBrains does not allow that. If you're interested in this missing feature, please upvote [IDEA-364676](https://youtrack.jetbrains.com/issue/IDEA-364676).
  * rework how the Chinese language is detected. This should avoid rare scenarios where the Chinese localization of the plugin was loaded on non-Chinese computers.
* integrates the latest version of Extra ToolWindow Colorful Icons (2025.1.1):
  * implement [#6](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/6): add colors to the `Show History` icon.
  * add colors to the `Bazel` tool window icon.
  * rework the `Add`, `Back`, `Bookmarks`, `Branch`, `Build`, `Close` (multiple icons), `Collapse`, `Collapse All`, `Changes` (VCS), `Commit`, `Database`, `Database Changes`, `Debug`, `Endpoints`, `Expand`, `Expand All`, `Fetch`, `Forward`, `Gradle`, `Learn` (Feature Trainer), `Maven`, `Merge`, `Profile`, `Redo`, `Remove`, `Run`, `Problems`, `Push`, `Reset`, `Rollback`, `Services`, `Show Diff`, `Spring`, `SQL Generator`, `Terminal`, `Undo`, `Update`, and `Writerside` tool window icons when using the New UI.
  * add colors to the `Chevron Up` and the `Chevron Down` normal and large icons.
  * some icons now have variants, similar to [alternative icons from Extra Icons](https://jonathanlermitage.github.io/ij-extra-tools-pack-docs/extra-icons-plugin-icons.html#alternative-icons).
  * the New UI theme has been reworked, and a third theme "New UI Remix" has been added, which looks like the New UI theme with more visible lines.
  * improve the Chinese localization.
  * rework how the Chinese language is detected. This should avoid rare scenarios where the Chinese localization of the plugin was loaded on non-Chinese computers.
* integrates the latest version of Extra IDE Tweaks (2025.1.1):
  * disable the `Always Excluded Folders` feature when loading projects with a huge number of modules (like IntelliJ Community sources, which has 1300 modules). The module limit is set to 20 to avoid any performance degradation. A future update will rework this feature.
  * rework the `Open Editors` tool window icon.
  * improve the search field at the top of the config panel. This should work much better.
  * minor code rework.
  * rework how the Chinese language is detected. This should avoid rare scenarios where the Chinese localization of the plugin was loaded on non-Chinese computers.
* [documentation](https://jonathanlermitage.github.io/ij-extra-tools-pack-docs/).

## 2024.13.1 (2024/12/13)
* integrates the latest version of Extra Icons (2024.10.1):
  * fix [#192](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/192): custom icons not working in Explorer tool window in Rider for C# project.
  * implement [#191](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/191): support `eslint.config.js` files.
  * implement [#191](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/191): support various [Stylelint](https://stylelint.io/user-guide/configure) files.
  * the [online documentation](https://jonathanlermitage.github.io/ij-extra-tools-pack-docs/) has been completely rewritten.
  * minor UI reworks in the settings panel.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.6.3):
  * minor UI reworks in the settings panel.
  * minor code reworks
* integrates the latest version of Extra IDE Tweaks (2024.18.1):
  * **Better Folder Icons** now supports the `(.)log(s)` folders from Extra Icons.
  * **Prevent Opening of Sensitive Files** now supports read-only files (2024.2+ IDEs only).

## 2024.12.2 (2024/11/19)
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.6.2):
  * hopefully fix `com.intellij.diagnostic.PluginException: Cannot init component state (...)` errors.
* integrates the latest version of Extra IDE Tweaks (2024.17.2):
  * hopefully fix `com.intellij.diagnostic.PluginException: Cannot init component state (...)` errors.

## 2024.12.1 (2024/11/16)
* integrates the latest version of Extra Icons (2024.9.1):
  * fix [#190](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/190): Extra Icons not configurable at project level. This was a regression from the previous plugin version. Sorry for the inconvenience.
  * support Embedded Open Type, TrueType Font, and Web Open Font Format font files.
  * add more alternative icons for `*.cmd`, `*.bat`, Powershell `*.ps1`, Bash `*.sh` files.
  * support Bash (without `.sh` extension) files.
  * rework the `*.env` file icon.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.6.1):
  * rework the Hierarchy toolbar icon.
  * rework the [Extra IDE Tweaks](https://plugins.jetbrains.com/plugin/23927-extra-ide-tweaks) Open Editors tool window icon.
  * rework the Writable and the Read-Only tool window icons when using the New UI.
  * add colors to the Persistence tool window icon.
  * add colors to the Android Resources Manager tool window icon.
  * add colors to the WriterSide Collapse All and Expand All icons in the WriterSide tool window. For now, this works with the New UI only. The Classic UI is affected by a bug (see [WRS-6459](https://youtrack.jetbrains.com/issue/WRS-6459)).
  * implement [#4](https://github.com/jonathanlermitage/intellij-extra-toolwindow-colorful-icons-pub/issues/4): add colors to the Tests tool window in Rider.
  * fix support of the editor tab pinned icon. No longer overrides the WriterSide "Pin the Preview" icon.
* integrates the latest version of Extra IDE Tweaks (2024.17.1):
  * **Properties** context menu: display file or folder properties (like size, number of files, etc.). 

## 2024.11.2 (2024/10/29)
* fix potential component ID collisions when installing this plugin alongside other obfuscated plugins.
* code rework: replace usage of obsolete JetBrains APIs, improving compatibility with future IDEs.

## 2024.11.1 (2024/10/21)
* integrates the latest version of Extra Icons (2024.8.1):
  * support `Makefile` files.
  * UI reworks in the settings panel.
  * minor code rework.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.5.3):
  * remove the unused third-party library Apache Commons IO.
* integrates the latest version of Extra IDE Tweaks (2024.16.1):
  * **Better Folder Icons** now supports the Kotlin Multiplatform OS folders from Extra Icons.
  * add **Commit Alert**: this inspection allows you to define keywords that will show a confirmation dialog before committing files containing any of those keywords. Per example, define the COMMIT_ALERT keyword, modify, delete or move one or multiple files containing it, then commit. A confirmation dialog will appear asking if you still want to commit.
  * add **Activate All Tool Windows**: this action activates all available tool windows in the current project. Enable it in settings, then see the `Window > Activate All Tool Windows` menu item. It's like clicking on the "..." button on the left-side toolbar, then clicking on each available tool window.
  * add options to show `Tools > Extra IDE Tweaks...` and `Tools > Plugins...` menu items.
  * settings: a search field has been added for quicker access to the parameters you are looking for.
  * minor UI reworks in the settings panel.
  * minor performance optimization.

## 2024.10.2 (2024/09/23)
* fix usage of some JetBrains deprecated APIs, improving the compatibility with future IDEs (2024.3+).
* integrates the latest version of Extra IDE Tweaks (2024.15.2):
  * rework the `Prevent Opening of Sensitive Files` feature. Because there is no official API for that, I was using a workaround, but recent IDE updates made it less reliable, making (sometimes) the file content visible during a brief instant. I found new workarounds that work with most IDE installations. BTW, these are still workarounds, and up-voting [IDEA-359327](https://youtrack.jetbrains.com/issue/IDEA-359327/Provide-an-API-to-prevent-file-opening) would greatly help.
  * reduce the plugin size by removing the dependency to Apache Commons IO and by using custom code from Java NIO instead.

## 2024.10.1 (2024/09/17)
* improve compatibility with future IDEs (2024.3+).
* integrates the latest version of Extra Icons (2024.7.2):
  * avoid some rare NPE errors when importing an old Extra Icons config at project level.
  * a recent bug in Extra Icons (2024.6.4, 2024/07/29) prevented icon override for files with multiple dots in their name. This is fixed now.
  * fix usage of some JDK deprecated APIs.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.5.1):
  * add colors to the AI Assistant status icon (status: disabled).
  * add colors to the Grazie Pro status icon (status: local processing).
  * rework AI Assistant and Grazie Pro tool window icons color. AI Assistant is green when enabled. Grazie Pro is green when using local processing and blue when connected to the cloud. Both are red when disabled or unavailable.
* integrates the latest version of Extra IDE Tweaks (2024.15.1):
  * add **Open as Project** to the folder's context menu from the Project tool window. The idea is to implement [IJPL-158161](https://youtrack.jetbrains.com/issue/IJPL-158161).
  * add the ability to have **default Excluded Folders** from indexing. There is now a global list of excluded folders. The idea is to implement [IJPL-8363](https://youtrack.jetbrains.com/issue/IJPL-8363).
  * **Better Tab Names**: add an option to remove the parenthesis after the file name if it's located in the root project or module. Per example, renames "build.gradle.kts (my-module)" to "build.gradle.kts". For now, it works with "build.gradle", "build.gradle.kts", "build.gradle.dcl", "settings.gradle", "settings.gradle.kts", "settings.gradle.dcl" and "src/main/resources/META-INF/plugin.xml" files only.
  * minor code rework.

## 2024.9.1 (2024/08/27)
* integrates the latest version of Extra IDE Tweaks (2024.14.1):
  * improve compatibility when the Python plugin (Ultimate or Community) is installed.
  * **Better Folder Icons**: add an icon for Python projects.
  * make the `Tools > Extra IDE Tweaks...` and `Tools > Plugins...` menu items available while indexing.
  * improve translations: replace "regular UI" with "classic UI".
* integrates the latest version of Extra Icons (2024.7.1):
  * improve compatibility when the Python plugin (Ultimate or Community) is installed.
  * rework Python icons (virtualenv, requirements.txt, wheel) and provide icons for the new UI.

## 2024.8.1 (2024/08/20)
* integrates the latest version of Extra IDE Tweaks (2024.13.1):
  * fix [#2](https://github.com/jonathanlermitage/intellij-extra-ide-tweaks/issues/2): `Prevent Opening of Sensitive Files` is broken in 2024.2+ IDEs.
  * avoid an invisible error when closing a project or the IDE. This error had no impact other than to pollute the IDE logs.
  * add an option to disable the plugin's features. Use it if you installed Extra Tools pack, but you don't want Extra IDE Tweaks features.
  * add an option to disable the Open Editors tool window.
  * improve translations.
  * translate the `Trusted Locations` and `Favorite Projects` menus in Chinese.
* integrates the latest version of Extra ToolWindow Colorful Icons (2024.4.1):
  * add colors to the Writerside icons.
  * rework the [PsiViewer](https://plugins.jetbrains.com/plugin/227-psiviewer) icon.

## 2024.7.2 (2024/08/02)
* **IMPORTANT**: avoid an IDE crash if you try to install both Extra Icons and Extra Tools Pack plugins. Before this fix, you had to delete one of the plugin files manually; otherwise the IDE would fail to start. Now, the IDE will disable both plugins and let you choose which one should be enabled. The best thing to do is to uninstall Extra Icons (and Extra IDE Tweaks and Extra ToolWindow Colorful Icons) first, so you can install Extra Tools Pack without any issues. Sorry for this annoying issue.

## 2024.7.1 (2024/07/29)
* integrates the latest version of Extra Icons (2024.6.4, 2024/07/29):
  * implement [#184](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/discussions/184):  support `.gitea` folders and `*.yml` files in `workflows` subdirectories.
  * fix [#183](https://github.com/jonathanlermitage/intellij-extra-icons-plugin/issues/183): custom icons should apply to files and folders only, not to class members like properties, methods, and nested classes.
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
