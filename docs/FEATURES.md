# OmniCleaner features

OmniCleaner 1.0.0 is a native Windows 11 maintenance application organized around six goal-oriented workspaces. The interface keeps common tasks obvious, advanced controls discoverable, and destructive actions gated behind preview and confirmation.

## Overview and navigation

- At-a-glance recoverable-space, candidate, drive, Recycle Bin, and activity cards.
- Guided Analyze → Review → Clean workflow.
- Categorized tool shortcuts for cleanup, storage, file finders, apps, Windows inventory, and automation.
- Global feature finder with `Ctrl+K` keyboard access.
- Mouse-over descriptions and accessibility help text for features and controls.
- Progressive disclosure for advanced settings and power tools.
- Local history, recovery state, and guard-status indicators.

## Cleanup & privacy

- 112 curated built-in cleaning rules.
- Windows temporary files, logs, dumps, thumbnails, delivery files, and supported maintenance caches.
- Chromium- and Firefox-family browser caches, crash data, storage, and recent traces where safe.
- Application caches for communication, productivity, creative, developer, launcher, and gaming software.
- Privacy-oriented recent-item, history, and trace rules with extra review guidance.
- Safe, caution, and advanced risk classifications.
- Per-rule search, filtering, source display, explanation, enablement, and result review.
- Exact candidate paths, sizes, modification dates, and planned actions.
- User-defined absolute-path exclusions applied to descendants.
- Supported-browser running-state warnings.
- Quick, Balanced, and Privacy profiles.

## Rules and extensibility

- Built-in rule catalog with deterministic identifiers and versioned definitions.
- Winapp-style definition imports.
- Native JSON rule schema.
- Integrated Rule Lab for authoring, validation, scope review, and import checks.
- Signed remote-catalog infrastructure using explicit HTTPS endpoints and digest/signature validation.
- No silent catalog or application update checks.

## Storage & files

### Storage analysis

- Folder-size and file-extension summaries.
- Whole-tree analysis with protected-path awareness.
- Results that avoid hydrating cloud placeholders.
- Storage snapshots and local trend history.

### Empty directories

- Recursive empty-directory discovery.
- Configurable inclusion and protection behavior.
- Preview before removal.
- Parent revalidation after child processing.
- Reparse-point and protected-root boundaries.

### Large files

- Configurable size threshold.
- Path, size, and detail review.
- Multi-folder scanning.
- Explicit selection before processing.

### Duplicate files

- Size-based candidate grouping.
- Sample hashing to reduce unnecessary full reads.
- Full SHA-256 verification.
- Final byte-for-byte confirmation.
- Per-group selection and conservative deletion behavior.

## Apps & Windows

- Installed desktop application inventory.
- Native uninstaller handoff rather than unattended removal.
- Startup-entry inventory for supported registry locations.
- Reversible enable/disable behavior for supported startup entries.
- Windows service and scheduled-task visibility.
- Windows Update inventory and native update handoff.
- Explicit WinGet package update checks and handoff.
- Driver inventory without automatic driver replacement.
- Browser-profile privacy and settings handoffs.
- Direct access to selected native Windows maintenance tools.

## Automation

- Quick, Balanced, and Privacy automation profiles.
- Windows Task Scheduler integration.
- Daily, weekly, and other supported schedules.
- Analyze-only mode.
- Cleanup-size budgets.
- Optional shutdown after a successful scheduled operation.
- Local outcome records and history.
- No resident service, tray application, or always-on monitor.
- Command-line workflows for scripted analysis, review, diagnostics, and storage reports.

## Recovery & portability

- Recycle Bin deletion as the recommended default.
- Quarantine mode with retention settings.
- Restore support for quarantined items.
- Permanent deletion only as an explicit setting.
- Local execution history and outcome details.
- Import/export settings bundles.
- Folder exclusions that travel with exported settings.

## Platform and footprint

- Windows 11-focused design.
- Native x64 and ARM64 packages.
- Lightweight idle behavior because nothing remains resident when the UI is closed.
- No account, advertising, analytics, telemetry, cloud storage, or online dashboard.
- No automatic updater or unsolicited network call.

## Intentionally excluded

OmniCleaner does not include a registry cleaner, fake performance score, automatic driver replacement, multi-pass SSD wiping, forced browser/process termination, RAM “boosting,” unattended app removal, or aggressive service-disable presets. See [Safety](SAFETY.md) for the reasoning.
