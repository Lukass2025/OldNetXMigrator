# Old Net X Migrator — Version History

Official version history and documented development milestones for Old Net X Migrator.

> **Release status:** Only versions listed under [GitHub Releases](https://github.com/Lukass2025/OldNetXMigrator/releases) are published releases. Some intermediate v3.4.x versions below were internal/QA test builds and were not separately published. Version numbers alone do not imply public availability.

---

## v4.0.0.0 — Secure Updates & Native Netscape Integration

**Public release — 27 October 2026.**

### Changes

1. Completed the security-focused updater architecture developed through the v3.4.x series.
2. Integrated **Find Updates → Updates → Install Updates → Restart Navigator** into Netscape's native Add-ons Manager flow.
3. Restored the classic Updates list, available-version display, and **Include this update** checkbox.
4. Improved performance by checking an authenticated version manifest before downloading any extension package.
5. Improved update-status reporting; clearer progress messaging during the download phase remained a focus for follow-up development.
6. Bundled a self-contained **.NET 10 Secure Update Bridge**; a separate .NET Runtime installation is not required for the distributed companion.
7. Preserved HTTPS certificate validation, pinned publisher public-key verification, **RSA-PSS/SHA-256 manifest signatures**, XPI SHA-256 integrity checks, and archive/package validation.
8. Avoided unnecessary XPI downloads when the installed version was already current; allowed only verified packages to be reused from cache.
9. Corrected the **No updates were found** result when no newer version is available.
10. Prevented a temporary Windows console window from appearing during update checks.
11. Preserved the classic migration notice, Mozilla Firefox link, Old Net X **Coming soon** notice, and existing extension functionality.
12. Prepared continued distribution and update testing through GitHub Releases.

> **Development note:** v4.0.0.0 carries forward the behavior tested in v3.4.2.4, without unrelated interface changes. Signed update verification does **not** make the legacy Netscape browser itself secure.

---

## v3.4.2.4 — Silent Update Checker Window Fix

**Development/test build; no separate public GitHub Release recorded.**

### Changes

1. Removed the brief black Windows console window that could appear during signed update checks.
2. Preserved the fast version-check path and native Netscape Add-ons update interface.
3. Retained the existing publisher-signature, HTTPS, SHA-256, and package-validation requirements.

---

## v3.4.2.3 — Faster Signed Update Discovery

**Development/test build; no separate public GitHub Release recorded.**

### Changes

1. Split initial signed version discovery from downloading and verifying a complete XPI.
2. Made **No updates were found** appear promptly when there is no newer version.
3. Deferred the more expensive package download and validation until a newer signed version had been detected.
4. Kept all required authenticity and integrity checks before an update could be installed.

---

## v3.4.2.2 — Integrated Update Workflow Test

**GitHub pre-release.**

### Changes

1. Continued testing of the integrated native Netscape Add-ons Manager update flow.
2. Used a signed update manifest and a verified XPI candidate for update installation testing.
3. Confirmed the restart-based extension update workflow during local testing.

> **Historical note:** The published release description identifies v3.4.2.2 as a test of **Find Updates**. This entry records development context; it should not be treated as a separately certified stable build.

---

## v3.4.2.1 — Native Find Updates Compatibility Fix

**Development/QA build.**

### Changes

1. Intercepted Netscape's original **Find Updates** command before the legacy RDF updater ran.
2. Improved delayed XUL initialization and inline update-status recovery.
3. Retained the native installation action only for verified newer packages.
4. Preserved RSA-PSS/SHA-256 signature and package-integrity verification.

---

## v3.4.2.0 — Native Add-ons Update Integration

**Development/QA pre-release build.**

### Changes

1. Improved presentation of authenticated update results inside Netscape's Add-ons Manager.
2. Reduced duplicate pop-ups and legacy update-check errors.
3. Introduced handling for an installation request involving a publisher-verified XPI.
4. Preserved user confirmation and security checks.

> **Development note:** The complete Netscape-native experience was still under live testing at this stage.

---

## v3.4.1.1 — Find Updates Integration Fix

**Development/QA build.**

### Changes

1. Improved detection of Netscape's **Find Updates** command, including legacy XUL button events and `cmd_update` variations.
2. Reduced duplicate checks when a click generated multiple related events.
3. Preserved the previously implemented signed update-verification model.

---

## v3.4.1.0 — Signed Update System & Netscape Integration

**GitHub pre-release.**

### Changes

1. Introduced a .NET 10 Secure Bridge for modern HTTPS update retrieval.
2. Added RSA-PSS/SHA-256 signature verification and publisher public-key pinning.
3. Added XPI integrity, version, compatibility, and archive-safety validation.
4. Added **Tools → Old Net X Migrator** update-checker and diagnostic commands.
5. Began integration with Netscape's built-in **Find Updates** functionality.
6. Recorded 17 security tests, 7 archive-safety tests, and 7 signature-rejection tests in the development release notes.

> **Development note:** The complete native installation workflow had not yet been fully validated.

---

## v3.4.0.1–v3.4.0.4 — Local Update & HTTPS Navigation Tests

**Private/local QA builds — not public GitHub Releases.**

### Development milestones

1. Tested Netscape's original Add-ons update workflow with a loopback-only local RDF server, including the v3.4.0.0 → v3.4.0.1 → v3.4.0.2 test sequence.
2. Confirmed that an already current local version returns **No updates were found**.
3. In v3.4.0.3, explicitly blocked user-entered HTTP addresses from being passed into the HTTPS-only WebView2 integration while preserving normal HTTPS navigation.
4. In v3.4.0.4, added local negative-path tests involving unavailable, incomplete, or incorrectly hashed update packages.

> **Historical note:** These isolated localhost experiments were development tools, **not** the public update mechanism. The final signed HTTPS architecture was introduced in subsequent versions.

---

## v3.4.0.0 — Secure Update Architecture Transition

**GitHub pre-release — documentation/development milestone; no public XPI installer was provided for this tag.**

### Changes

1. Began the transition toward independently authenticated extension updates.
2. Removed the experimental unsecured localhost HTTP update endpoint and its associated configuration.
3. Removed the unsigned legacy `update.rdf` approach from the release candidate.
4. Updated extension identification and version metadata.
5. Refined compatibility declarations for Netscape Navigator 9.0.0.6.
6. Removed the unverified Firefox 2 compatibility declaration.
7. Updated migration-interface text and removed obsolete development instructions.
8. Preserved the established classic migration and integrated browser features.

---

## v3.3.2.0 — Startup Notification Reliability Fix

### Changes

1. Fixed the *End of Support* dialog appearing only once after installation.
2. Restored automatic notification display on every new Netscape startup.
3. Removed the persistent `welcomeShown` preference as a startup blocker.
4. Prevented duplicate notifications within the same browser session.
5. Preserved the **Don't show again** option.
6. Allowed **Remind me later** to re-enable startup notifications.

---

## v3.3.1.0 — Alpha Development & Coming Soon Notice

### Changes

1. Disabled the **Download Old Net X** link while the browser remains in active Alpha development.
2. Replaced the active blue download link with a disabled gray label and added a **Coming soon...** indicator.
3. Added a clear explanation that Old Net X is still under active development and is not yet publicly available for download.
4. Introduced an announcement informing users that a future Migrator update will provide information about the first public Beta test release and continued browser development.
5. Removed navigation to the temporary `oldnetx.lv` placeholder to prevent users from opening an unavailable download page.
6. Preserved the fully functional Mozilla Firefox download link, directing users to Mozilla's official website.
7. Updated the first-run notification for version 3.3.1.0, ensuring the revised Alpha development notice appears after installation and browser restart.

---

## v3.3.0.0 — Interface & Startup Improvements

### Changes

1. Restored automatic display of the *End of Support* dialog after installing or updating the extension and restarting Netscape.
2. Fixed an issue where settings saved by previous versions prevented the welcome dialog from appearing.
3. Added support for opening recommendation links in the original browser tab when it is still empty and unused.
4. Preserved new-tab navigation when the original tab is already in use.
5. Replaced the default Add-ons icon with the original Old Net X icon.
6. Replaced the Netscape icon in the Migrator window with the original Old Net X icon.
7. Integrated original 32×32 and 64×64 icon resources to improve visual quality.

---

## v3.2.0.0 — Navigation Reliability Fixes

### Changes

1. Fixed the issue where recommendation links could open an empty **Untitled** tab.
2. Improved synchronization between Netscape's tab creation and WebView2 initialization.
3. Added a mechanism that waits until the new tab is ready before starting navigation.
4. Improved automatic NPAPI plugin initialization within newly opened tabs.
5. Added error handling when WebView2 cannot initialize successfully.
6. Updated the Migrator window's title-bar behavior.

---

## v3.1.0.0 — Browser Integration & Visual Improvements

### Changes

1. Changed recommendation-link behavior to open websites in Netscape Navigator tabs instead of a separate Migrator window.
2. Updated the Mozilla Firefox logo to a newer official version.
3. Improved the Old Net X logo's resolution and appearance.
4. Updated the red exclamation-mark icon in the browser's status bar to better match the original Netscape design.
5. Improved the appearance and proportions of the *End of Support* dialog.

> **Development note:** The new-tab implementation introduced an empty-tab issue that was subsequently addressed in v3.2.0.0.

---

## v3.0.0.0 — MAJOR RELEASE

### Unified Extension & WebView2 Integration

**The most significant milestone in Old Net X Migrator development.**

Version **3.0.0.0** marked a major architectural transformation. Three previously separate components were combined into a single, integrated Netscape Navigator extension.

### Three Projects — One Extension

#### 1. Old Net X Migrator

- Integrated the classic *End of Support* dialog inspired by Netscape's original 2008 migration interface.
- Added recommendations for Old Net X and Mozilla Firefox.
- Integrated browser logos, descriptions, and download-page links.
- Added **Don't show again** and **Remind me later** options.
- Added the red exclamation-mark notification icon to the Netscape status bar.
- Enabled reopening the Migrator dialog by clicking the notification icon.

#### 2. NPAPI WebView2 Bridge

- Integrated the native 32-bit `npOldNetXWebView2Bridge.dll` plugin.
- Enabled modern websites to be rendered using Microsoft Edge WebView2 inside Netscape Navigator.
- Preserved support for modern web content, including video playback, audio, and fullscreen operation.
- Removed the need to distribute the NPAPI bridge as a separate Old Net X component.

#### 3. Browser Navigation Integration

- Integrated the previously developed **v0.2.1 WebView2 navigation extension**.
- Connected Netscape's original address bar to the modern rendering engine.
- Preserved **Back**, **Forward**, **Refresh**, and other navigation commands.
- Enabled WebView2 content to operate within Netscape browser tabs.
- Eliminated the requirement to manually open separate HTML test files for normal navigation.

### Unified Installation

- Combined the Migrator interface, navigation integration, and NPAPI plugin into **one `.xpi` installation package**.
- Simplified installation and future updates.
- Established a unified architecture for subsequent Migrator releases.

### Major Milestone

> **Old Net X Migrator evolved from a standalone migration dialog into an integrated extension connecting the original Netscape Navigator interface with a modern WebView2 rendering engine.**

---

## v2.0.0.0 — Initial Functional XUL Extension

### Changes

1. Created an installable XUL/XPI extension for Netscape Navigator 9.0.0.6.
2. Implemented extension identification and registration in the Add-ons Manager.
3. Added integration with Netscape's **Tools** menu.
4. Enabled the Migrator dialog to be opened directly from the browser.
5. Established the initial structure for the classic migration interface.
6. Laid the foundation for future browser recommendations and migration features.

### Development Status

**Functional interface prototype.**

Download links, bookmark migration, and WebView2 integration were not yet implemented as a unified solution.

---

## v1.0.0.0 — Initial Development Stage

### Changes

1. Earliest stage of the Old Net X Migrator project.
2. The project was based on the concept of preserving and modernizing Netscape's classic *End of Support* migration experience.
3. Detailed implementation records for this version have not been confirmed.

### Historical Note

> The exact feature set and release status of v1.0.0.0 remain undocumented. This entry should be updated if the original source code or installation package becomes available.
