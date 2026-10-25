v3.3.2.0 – Startup Notification Reliability Fix

1.) Fixed the End of Support dialog appearing only once after installation.
2.) Restored automatic notification display on every new Netscape startup.
3.) Removed the persistent welcomeShown preference as a startup blocker.
4.) Prevented duplicate notifications within the same browser session.
5.) Preserved the "Don't show again" option.
6.) Allowed "Remind me later" to re-enable startup notifications.
7.) Preserved the existing NPAPI WebView2 bridge and navigation system.

---

v3.3.1.0 – Alpha Development & Coming Soon Notice

1.) Disabled the "Download Old Net X" link while the browser remains in active Alpha development.
2.) Replaced the active blue download link with a disabled gray label and added a "Coming soon..." indicator.
3.) Added a clear explanation that Old Net X is still under active development and is not yet publicly available for download.
4.) Introduced an announcement informing users that a future Migrator update will provide information about the first public Beta test release and continued browser development.
5.) Removed navigation to the temporary oldnetx.lv placeholder to prevent users from opening an unavailable download page.
6.) Preserved the fully functional Mozilla Firefox download link, directing users to Mozilla's official website.
7.) Updated the first-run notification for version 3.3.1.0, ensuring the revised Alpha development notice appears after installation and browser restart.
8.) Preserved the existing NPAPI WebView2 bridge, browser navigation functionality, original icons, and classic Netscape interface integration.

---

v3.3.0.0 — Interface & Startup Improvements

1.) Restored automatic display of the *End of Support* dialog after installing or updating the extension and restarting Netscape.
2.) Fixed an issue where settings saved by previous versions prevented the welcome dialog from appearing.
4.) Added support for opening recommendation links in the original browser tab when it is still empty and unused.
5.) Preserved new-tab navigation when the original tab is already in use.
6.) Replaced the default Add-ons icon with the original Old Net X icon.
7.) Replaced the Netscape icon in the Migrator window with the original Old Net X icon.
8.) Integrated original 32×32 and 64×64 icon resources to improve visual quality.
9.) Preserved the existing WebView2 navigation bridge.

---

v3.2.0.0 — Navigation Reliability Fixes

1.) Fixed the issue where recommendation links could open an empty **Untitled** tab.
2.) Improved synchronization between Netscape's tab creation and WebView2 initialization.
3.) Added a mechanism that waits until the new tab is ready before starting navigation.
4.) Improved automatic NPAPI plugin initialization within newly opened tabs.
5.) Added error handling when WebView2 cannot initialize successfully.
6.) Updated the Migrator window's title-bar behavior.
7.) Preserved the existing address-bar and browser navigation functionality.

---

v3.1.0.0 — Browser Integration & Visual Improvements

1.) Changed recommendation-link behavior to open websites in Netscape Navigator tabs instead of a separate Migrator window.
2.) Updated the Mozilla Firefox logo to a newer official version.
3.) Improved the Old Net X logo's resolution and appearance.
4.) Updated the red exclamation-mark icon in the browser's status bar to better match the original Netscape design.
5.) Improved the appearance and proportions of the *End of Support* dialog.
6.) Preserved the integrated NPAPI WebView2 bridge.

Note: The new-tab implementation introduced an empty-tab issue that was subsequently addressed in v3.2.0.0.

---

v3.0.0.0 — MAJOR RELEASE
Unified Extension & WebView2 Integration

The most significant milestone in Old Net X Migrator development.

Version 3.0.0.0 marked a major architectural transformation. Three previously separate components were combined into a single, integrated Netscape Navigator extension.

Three Projects — One Extension

1. Old Net X Migrator

1.1) Integrated the classic *End of Support* dialog inspired by Netscape's original 2008 migration interface.
1.2) Added recommendations for Old Net X and Mozilla Firefox.
1.3) Integrated browser logos, descriptions and download-page links.
1.4) Added **Don't show again** and **Remind me later** options.
1.5) Added the red exclamation-mark notification icon to the Netscape status bar.
1.6) Enabled reopening the Migrator dialog by clicking the notification icon.

2. NPAPI WebView2 Bridge

2.1) Integrated the native 32-bit `npOldNetXWebView2Bridge.dll` plugin.
2.2) Enabled modern websites to be rendered using Microsoft Edge WebView2 inside Netscape Navigator.
2.3) Preserved support for modern web content, including video playback, audio and full screen operation.
2.4) Removed the need to distribute the NPAPI bridge as a separate Old Net X component.

3. Browser Navigation Integration

3.1) Integrated the previously developed v0.2.1 WebView2 navigation extension.
3.2) Connected Netscape's original address bar to the modern rendering engine.
3.3) Preserved Back, Forward, Refresh and other navigation commands.
3.4) Enabled WebView2 content to operate within Netscape browser tabs.
3.5) Eliminated the requirement to manually open separate HTML test files for normal navigation.

Unified Installation

- Combined the Migrator interface, navigation integration and NPAPI plugin into one .xpi installation package**.
- Simplified installation and future updates.
- Established a unified architecture for subsequent Migrator releases.

Major milestone: Old Net X Migrator evolved from a standalone migration dialog into an integrated extension connecting the original Netscape Navigator interface with a modern WebView2 rendering engine.

---

v2.0.0.0 — Initial Functional XUL Extension

1.) Created an installable XUL/XPI extension for Netscape Navigator 9.0.0.6.
2.) Implemented extension identification and registration in the Add-ons Manager.
3.) Added integration with Netscape's Tools menu.
4.) Enabled the Migrator dialog to be opened directly from the browser.
5.) Established the initial structure for the classic migration interface.
6.) Laid the foundation for future browser recommendations and migration features.

Development stage: Functional interface prototype. Download links, bookmark migration and WebView2 integration were not yet implemented as a unified solution.

---

v1.0.0.0 — Initial Development Stage

1.) Earliest stage of the Old Net X Migrator project.
2.) The project was based on the concept of preserving and modernizing Netscape's classic *End of Support* migration experience.
3.) Detailed implementation records for this version have not been confirmed.

Historical note: The exact feature set and release status of v1.0.0.0 remain undocumented. This entry should be updated if the original source code or installation package becomes available.
