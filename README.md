# Old Net X Migrator

**A classic Netscape Navigator 9 extension, migration notice, and experimental WebView2 integration project.**

Old Net X Migrator is an independent preservation and development project for **Netscape Navigator 9.0.0.6**. It combines a classic-style end-of-support/migration dialog, an experimental NPAPI-to-WebView2 integration, and a signed extension-update workflow that uses Netscape's familiar Add-ons Manager interface.

> [!WARNING]
> **Netscape Navigator 9 is obsolete and is not a secure modern browser.** Old Net X Migrator does not patch Netscape, modernize its entire engine, or make it safe for sensitive accounts, payments, or everyday browsing. Use the project in an isolated test environment and at your own risk.

## Project at a glance

| | |
| --- | --- |
| Latest public release | [v4.0.0.0](https://github.com/Lukass2025/OldNetXMigrator/releases/tag/v4.0.0.0) |
| Target application | Netscape Navigator 9.0.0.6 (32-bit) |
| Tested operating system | Windows 11 x64 |
| Modern rendering component | Microsoft Edge WebView2 Evergreen Runtime |
| Release format | `.xpi` extension package |
| Development model | Independent, experimental; proprietary software |
| Download | [GitHub Releases](https://github.com/Lukass2025/OldNetXMigrator/releases) |

## What does it do?

### 1. Classic migration and end-of-support notice

- Displays a migration/end-of-support dialog inspired by Netscape's original interface.
- Offers a link to Mozilla Firefox's official website.
- Provides a notice about **Old Net X**, a separate browser project that is still under development; its download option is intentionally marked **Coming soon**.
- Includes the classic notification icon, startup-notice preferences, and a way to reopen the dialog.

The name *Migrator* refers to this migration experience. **It does not currently transfer bookmarks, saved passwords, browser profiles, or other personal data to another browser.**

### 2. Experimental WebView2 bridge

The extension bundles a 32-bit NPAPI integration component that can display selected modern web content through **Microsoft Edge WebView2** within the classic Netscape interface. Navigation integration includes familiar browser actions such as Back, Forward, and Refresh.

This is an **experimental compatibility bridge**, not a replacement for Netscape's underlying browser engine. Website behavior, audio/video, fullscreen, and navigation may vary; compatibility with every website is **not** guaranteed. WebView2 does not remove vulnerabilities elsewhere in the legacy browser or its plugin architecture.

### 3. Signed extension updates

Starting with the v3.4.x development work and completed for the v4.0.0.0 release, Old Net X Migrator uses an integrated, self-contained Windows update companion rather than an unsigned legacy update feed.

1. In Netscape, open **Tools → Add-ons → Extensions → Find Updates**.
2. The updater retrieves the update metadata over HTTPS and authenticates the signed manifest against the embedded trusted publisher public key.
3. It checks the available version. If no newer version exists, **No updates were found** is reported without downloading an XPI.
4. If a newer version exists, it downloads the candidate and verifies its integrity, extension identity, compatibility, and package structure before offering it for installation.
5. Netscape's **Updates → Install Updates → Restart Navigator** flow remains under the user's control.

Security checks include **RSA-PSS/SHA-256 manifest signatures**, publisher public-key pinning, HTTPS certificate validation, XPI SHA-256 checks, and archive validation. No update should be installed without successful verification and user confirmation. The bundled .NET 10 companion is self-contained; installing the .NET Runtime separately is not required for the distributed update component.

## Installation

1. Use a test system with **Windows 11 x64**, **Netscape Navigator 9.0.0.6**, and the **Microsoft Edge WebView2 Evergreen Runtime**.
2. Download the `.xpi` file from the [official GitHub release](https://github.com/Lukass2025/OldNetXMigrator/releases/tag/v4.0.0.0). Do not substitute a GitHub-generated *Source code (zip)* archive for the installer.
3. Install the XPI through Netscape Navigator's Add-ons installation interface.
4. Restart Netscape when prompted, then check **Tools → Add-ons → Extensions** for Old Net X Migrator.
5. If you choose to test updates, use **Find Updates** and confirm installation through Netscape's own interface.

Previous release packages are retained for development history. They may have different update capabilities or installation requirements. See the release notes for the specific version you use.

## Known limitations and important distinctions

- **Old Net X Migrator is not Old Net X.** Old Net X is a separate browser under development; this extension does not install it.
- **Not a security product.** The modern rendering component and signed updater do not make unsupported Netscape safe for general internet use.
- **Not a full migration tool.** Automated transfer of profiles, passwords, and bookmarks is not implemented.
- **Not an official Netscape, Mozilla, or Microsoft release.** Trademarks and product names belong to their respective owners.
- **Not a cross-platform compatibility promise.** The documented, tested configuration is Windows 11 x64 with Netscape 9.0.0.6; other environments are not certified here.
- **Not silent auto-installation.** Updates require user action through the Add-ons Manager.

## Version history

See [CHANGELOG.md](CHANGELOG.md) for release and development milestones, and [GitHub Releases](https://github.com/Lukass2025/OldNetXMigrator/releases) for downloadable public builds. Some intermediate versions in the changelog were local QA/development builds and were **not necessarily published as GitHub Releases**.

## Reporting bugs and suggesting improvements

Use [GitHub Issues](https://github.com/Lukass2025/OldNetXMigrator/issues) for reproducible bug reports, compatibility observations, and feature suggestions. Include the extension version, Netscape version, Windows version, expected behavior, observed behavior, and steps to reproduce. **Do not post passwords, secret signing keys, or security-sensitive exploit details publicly.** See [SECURITY.md](SECURITY.md) and [CONTRIBUTING.md](CONTRIBUTING.md).

## Source availability and licensing

This public repository is for project information, release history, distribution, and issue tracking. **It is not an open-source code repository.** The downloadable XPI may contain scripts and resources needed for the extension to run; their presence does not imply permission to reuse or redistribute them.

The project's software is proprietary. See [LICENSE.md](LICENSE.md) for the intended binary-use terms once those terms have been approved and published by the copyright holder. Third-party software and trademarks remain subject to their respective rights.

---

**Project author:** Lūkass Ernests Kļaviņš · Independent Old Net X project
