# Security Policy

## Important warning about Netscape Navigator 9

Netscape Navigator 9.0.0.6 is an unsupported legacy browser. Old Net X Migrator is an **experimental extension**, not a security upgrade for Netscape. Even when selected content is rendered using Microsoft Edge WebView2, Netscape's original browser and extension infrastructure still carry historical risks.

**Do not use this project for banking, payments, password management, work accounts, or other sensitive activity.** Prefer a current, supported browser for ordinary internet use, and perform Netscape testing in an isolated environment.

## Update security model

In current v4.x builds, update metadata is retrieved over HTTPS. The updater authenticates the publisher-signed manifest using an embedded trusted public key; compares versions before downloading; and checks the XPI hash, relevant metadata, and package safety before handing an eligible update to Netscape's user-confirmed installation workflow.

These checks are intended to protect **extension updates**. They are not a guarantee that Netscape Navigator, arbitrary web pages, or the broader host system are secure.

## Supported configurations

| Component | Documented test configuration |
| --- | --- |
| Extension | Latest published v4.x release |
| Browser | Netscape Navigator 9.0.0.6 (32-bit) |
| Operating system | Windows 11 x64 |
| Modern content runtime | Microsoft Edge WebView2 Evergreen |

Older releases and other operating systems are not covered by a security-support commitment. No security patching or response-time SLA is promised.

## Reporting a vulnerability

- **Do not post exploit code, credentials, private keys, or detailed unpatched security weaknesses in a public GitHub Issue.**
- Contact the repository maintainer privately through a contact method provided on their GitHub profile, or use GitHub's **Private vulnerability reporting** feature if it is enabled for this repository.
- Include the affected version, a concise impact description, and reproduction steps without exposing unrelated private data.

Please allow time for assessment before public disclosure. This is an independent experimental project, and no response or remediation deadline is guaranteed.

## What is not a vulnerability in the extension

General known weaknesses in the unsupported Netscape browser, unrelated plugins, or third-party websites should not be represented as vulnerabilities fixed or introduced by Old Net X Migrator unless a specific interaction has been demonstrated.
