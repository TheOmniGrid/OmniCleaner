# Frequently asked questions

## Is OmniCleaner open source?

No. OmniCleaner is currently proprietary. This repository publishes product information, screenshots, safety/privacy documentation, and support materials—not application source code.

## Where is the installer?

Installers and portable builds are deliberately not hosted on GitHub. See [Installation](INSTALLATION.md) for official channels.

## Does OmniCleaner run in the background?

No resident service, tray process, or always-on monitor is installed. If you configure automation, OmniCleaner uses Windows Task Scheduler to start a bounded run at the chosen time.

## Does it collect telemetry?

No. There is no account, analytics, advertising, or cloud backend. See [Privacy](PRIVACY.md).

## Can I see what will be removed?

Yes. Analysis is read-only and produces a per-item plan with paths, sizes, sources, dates, risk labels, and intended actions. Cleanup remains gated until a reviewable plan exists.

## Can cleanup be undone?

Recycle Bin is the recommended default. Quarantine and restoration are available for supported actions. Permanent deletion is explicit and should be used cautiously.

## Does it clean the registry?

No. Bulk registry cleaners offer little dependable value on current Windows systems and can introduce difficult-to-diagnose failures.

## Does it update drivers automatically?

No. OmniCleaner can inventory drivers and expose appropriate Windows-native paths, but it does not replace drivers automatically.

## How are duplicate files verified?

Candidates are grouped by size, screened with samples, verified with full SHA-256, and finally compared byte for byte. The user still decides what to remove.

## What happens with OneDrive or other cloud placeholders?

Storage analysis is designed to avoid hydrating cloud placeholders merely to measure them. Results depend on the metadata Windows and the provider expose locally.

## Can I add custom cleaning rules?

OmniCleaner supports Winapp-style imports, its native rule format, and an integrated Rule Lab. Imported definitions should always be reviewed, validated, and obtained from a trusted source.

## Which Windows versions are supported?

Version 1.0.0 focuses on modern Windows 11 machines on x64 and ARM64.
