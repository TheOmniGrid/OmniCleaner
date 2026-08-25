# Getting OmniCleaner

## Requirements

- Windows 11.
- x64 or ARM64 processor.
- A standard user account for normal scans; Windows may request elevation only when an explicitly selected native operation requires it.

## Release channels

OmniCleaner builds are distributed outside GitHub through official OmniGrid channels:

- [The OmniGrid on Patreon](https://www.patreon.com/TheOmniGrid)
- [The OmniGrid on Ko-fi](https://ko-fi.com/theomnigrid)

This GitHub repository is a product showcase, documentation center, support hub, and issue tracker. It intentionally contains no installer, executable, portable build, archive, or source package.

## Before installing

- Obtain builds only from a channel linked by The OmniGrid.
- Confirm that the product name and version match the release announcement.
- Keep Windows security protections enabled.
- Do not trust third-party “repacked,” “cracked,” or mirrored copies.

## Release integrity

Current 1.0.0 engineering packages include SHA-256 manifests, but Authenticode signing remains dependent on the publisher's protected certificate workflow. Until a signed channel is announced, compare the release hash with the value published through the same trusted official channel and do not treat a SmartScreen prompt—or its absence—as proof of authenticity.

The x64 installer/installed-CLI/dedicated-uninstaller lifecycle and package residue checks passed on the release validation machine. ARM64 package hashes and PE architecture were verified by cross-publish; execution on physical Windows 11 ARM64 hardware remains an explicit external validation item.

## First run

1. Open **Overview** and use the categorized workspace cards to understand the available tools.
2. Select **Cleanup & privacy**, review the enabled Balanced-profile rules, and choose **Analyze selected**.
3. Inspect the candidate list before enabling **Clean selected**.
4. Leave deletion mode set to **Recycle Bin (recommended)** until you are comfortable with the workflow.
5. Add folder exclusions in **Settings & safety** for anything that should never be scanned by smart cleanup.

The core workflow is intentionally safe to explore because analysis does not modify the system.
