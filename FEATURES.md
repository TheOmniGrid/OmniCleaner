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
- Clear Why and Expected-impact fields, safe-selection controls, aggregate warnings, and selected-file lock-owner reporting without process termination.
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
- Reusable multi-root scan sets, recurring extension-growth sources, logical and allocated-byte totals, compressed/sparse metadata, NTFS file identity, hard-link counts, and hard-link-aware physical totals.
- Cloud-footprint state from metadata without opening online-only placeholders.

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
- Hard-link alias suppression, deterministic keeper suggestions, and enforcement that at least one physical copy remains.

### Similar photos

- Local-only perceptual dHash grouping with the highest-resolution representative.
- Nothing is preselected, and similarity is never treated as exact duplication.
- Online-only placeholders are not hydrated; inputs above 64 MiB or 100 megapixels are refused, and hashing uses a bounded decode.

## Apps & Windows

- Installed desktop application inventory.
- Native uninstaller handoff rather than unattended removal.
- Startup-entry inventory for supported registry locations.
- Reversible enable/disable behavior for supported startup entries.
- Windows service and scheduled-task visibility.
- Windows Update inventory and native update handoff.
- Explicit WinGet package update checks and handoff.
- Driver inventory without automatic driver replacement.
- Read-only Microsoft Store/MSIX package inventory with Windows-owned uninstall handoff.
- Read-only Chromium and Firefox extension inventory with browser-owned removal and permission controls.
- Protected cookie domains that prevent broad cookie-database rules, plus native per-site privacy handoffs.
- Exact, reviewable multi-package WinGet plans with sequential execution, cancellation, and per-package outcomes—never wildcard, force, silent-uninstall, or reboot switches.
- Browser-profile privacy and settings handoffs.
- Direct access to selected native Windows maintenance tools.

## Windows 11 Care

- Update readiness with system-drive free space, pending-restart indicators, and `Windows.old` rollback footprint.
- Ranked Low Storage Rescue plans that keep each proposed action reviewable instead of inventing a health score.
- Downloads review for installers, archives, disk images, interrupted downloads, age, and size; personal files and cloud-only placeholders are never preselected.
- Read-only shortcut inspection that separates missing local targets from web/external targets. UNC and mapped-network targets are never probed, preventing analysis-driven SMB authentication.
- Microsoft-supported DISM Component Store analysis with output bounded to 4 MiB per stream; WinSxS content is never edited directly.
- Reversible per-user `Analyze with OmniCleaner` Explorer command without a shell-extension DLL, service, or machine-wide registration.
- Path-free, SHA-256-addressed diagnostics ZIPs that are never uploaded automatically.
- Containment-checked local Omni-suite discovery with explicit selection and no launch while OmniCleaner is elevated.

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
- Power-aware idle, AC-start, battery-stop, missed-run, runtime-limit, and transient completion-notification controls.

## Recovery & portability

- Recycle Bin deletion as the recommended default.
- Quarantine mode with retention settings.
- Restore support for quarantined items.
- Permanent deletion only as an explicit setting.
- Local execution history and outcome details.
- Import/export settings bundles.
- Folder exclusions that travel with exported settings.
- SHA-256 quarantine integrity checks, visible undo/expiry state, retention days, and collision-safe restoration.

## Platform and footprint

- Windows 11-focused design.
- Native x64 and ARM64 packages.
- Lightweight idle behavior because nothing remains resident when the UI is closed.
- No account, advertising, analytics, telemetry, cloud storage, or online dashboard.
- No automatic updater or unsolicited network call.

## Release assurance

- 49/49 deterministic Core tests, both WPF smoke targets, and CLI doctor/rule/storage gates pass for 1.0.0.
- The x64 installer, installed CLI, dedicated uninstaller, and no-residue lifecycle pass end to end.
- x64 and ARM64 self-contained packages, portable archives, SHA-256 manifests, versions, PE architecture, and icon roles were regenerated and verified.
- A standard security scan's single medium UNC-authentication finding was remediated and regression-tested; no critical, high, or medium finding remains open.
- Authenticode, broad fresh-VM coverage, physical ARM64 execution, accessibility/user review, and measured ETW performance remain external release-assurance tasks rather than unimplemented product features.

## Intentionally excluded

OmniCleaner does not include a registry cleaner, fake performance score, automatic driver replacement, multi-pass SSD wiping, forced browser/process termination, RAM “boosting,” unattended app removal, or aggressive service-disable presets. See [Safety](docs/SAFETY.md) for the reasoning.
