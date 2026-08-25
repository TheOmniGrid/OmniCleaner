# Changelog

All notable public OmniCleaner documentation and product milestones are recorded here.

## Unreleased

- No product changes are currently queued for publication.
- Documentation corrections and future release notes will be added here before publication.

## 1.0.0 — 2026-08-23

### Interface and product identity

- Introduced the Windows 11-focused Omni desktop interface with goal-oriented workspaces, an at-a-glance dashboard, and the guided Analyze → Review → Clean flow.
- Added global `Ctrl+K` feature search, categorized navigation, progressive disclosure, mouse-over explanations, accessibility help text, keyboard navigation, high-contrast resources, and virtualized result grids.
- Added local window/workspace continuity and complete interface support for
  English, German, Spanish, French, Romanian, Russian, Simplified Chinese,
  Japanese, Korean, and Turkish; missing feature-specific strings fall back
  safely to English.
- Finalized the OmniCleaner visual identity: complete color application/installer icon, broom-only window/taskbar mark, and matching grayscale uninstaller icon with deterministic Windows icon sizes.
- Corrected curved-window corner composition, internal resize zones, small-icon rendering, category artwork, and optical centering of the three guided-workflow numerals.

### Cleanup, privacy, and definitions

- Shipped 112 curated Windows, browser, application, communication, gaming, creative, graphics, developer, and privacy rules with risk, rebuild-cost, warning, detection, exclusion, and automation metadata.
- Added read-only analysis, exact candidate review, per-item selection, search/risk filtering, safe-selection controls, JSON report export, and immutable cleanup plans that are revalidated immediately before execution.
- Added protected-root, UNC, reparse-point, cloud-placeholder, active-browser, changed-item, and cleanup-budget safeguards.
- Added Winapp-style imports, a versioned native JSON format, settings/profile bundles, and the integrated Rule Lab with a visual builder, raw JSON, resolved targets, and read-only test previews.
- Added explicit signed online and offline catalogue workflows with byte limits, SHA-256, schema validation, RSA-PSS signatures, rollback/identity controls, and disabled-by-default imported rules. No endpoint is contacted automatically.

### Storage and file intelligence

- Added recursive empty-directory discovery, wildcard name filters, zero-byte/hidden/age options, bottom-up revalidation, and protected-root/reparse safeguards.
- Added configurable large-file discovery and Storage Intelligence 2 with multi-root scan sets, folder/extension summaries, bounded top files, treemap, local trends, logical/on-disk allocation, compressed/sparse metadata, hard-link identity, and cloud state without placeholder hydration.
- Added duplicate identification using size grouping, front/back samples, full SHA-256, final byte comparison, hard-link alias suppression, deterministic keepers, and a guarantee that at least one physical copy remains.
- Added local similar-photo review using bounded perceptual hashing. Files over 64 MiB or images over 100 megapixels are refused, nothing is preselected, and visual similarity is never treated as byte identity.

### Windows 11 Care, apps, and recovery

- Added update/reboot/rollback readiness, Low Storage Rescue planning, Downloads classification, shortcut health, supported DISM Component Store analysis, path-free diagnostics, reversible per-user Explorer integration, and contained local Omni-suite discovery.
- Added installed desktop app, Store/MSIX, startup, service, scheduled task, driver, browser-profile, and browser-extension inventories with native Windows/vendor handoffs where direct mutation would be unsafe.
- Added reversible registry and Startup-folder controls, protected cookie domains, Windows Restart Manager lock-owner reporting, and exact reviewed WinGet batch plans with cancellation and per-package outcomes.
- Added Recycle Bin default deletion, managed quarantine, SHA-256 integrity checks, retention/expiry state, collision-safe restore, exact history, and explicit permanent mode.
- Hardened Shortcut Health so UNC and mapped-network targets are never probed, preventing analysis-driven SMB authentication. Omni-suite launch is refused while OmniCleaner is elevated, and DISM output is bounded to 4 MiB per stream.

### Automation, command line, and distribution

- Added Quick, Balanced, and Privacy profiles plus least-privilege Windows Task Scheduler jobs with analyze-only, cleanup budgets, idle/AC/battery/missed-run/runtime controls, optional notification, and success-only shutdown—without a resident service or tray process.
- Added the headless CLI for analysis, confirmation-gated cleanup, rule/catalogue operations, storage reports, history, quarantine, profiles, and diagnostics.
- Added a separate-key manual signed application-update manifest check. OmniCleaner never checks, downloads, or installs application updates automatically.
- Produced self-contained Windows 11 x64 and ARM64 installer, uninstaller, and portable deliverables with SHA-256 manifests. The public repository intentionally contains none of those binaries or the application source.

### Final validation and security

- Passed 49/49 deterministic Core tests, both WPF smoke targets, and CLI doctor/rule/storage gates.
- Passed the complete x64 quiet install, installed-CLI, dedicated-uninstaller, and no-residue lifecycle; regenerated and verified x64/ARM64 hashes, versions, architecture, and embedded icon roles.
- Completed a standard security scan. Its single medium UNC-authentication finding was remediated and regression-tested after the sealed snapshot; no critical, high, or medium finding remains open.
- Documented the remaining external assurance work: Authenticode signing, broader fresh-VM coverage, physical ARM64 execution, accessibility/user review, ETW measurements, socket-bound DNS validation, hostile-image codec testing, and handle-bound mutation before any future elevated mode.

### Public repository and presentation

- Built a source-free public product repository with an Omni-style animated header, product badges, quick-navigation buttons, curated screenshots, capability and safety graphics, brand assets, and matching Patreon/Ko-fi support buttons.
- Added complete public feature, coverage, safety, privacy, installation, FAQ, support, security, contribution, licensing, third-party notice, press-kit, and repository-scope documentation.
- Added defensive publication policy and validation that exclude application source, definitions, tests, scripts, binaries, installers, archives, signing material, and private build infrastructure from GitHub.
- Reconciled the public feature and safety claims with the final 1.0.0 engineering record, including the last security fixes, package gates, and clearly separated external assurance work.

### Deliberate product boundaries

- Registry cleaning, arbitrary cleanup scripts, forced process termination, unattended uninstall, autonomous driver replacement, fake health scores, resident monitoring, credentialed cloud cleaners, telemetry, advertising, and claimed multi-pass SSD wiping remain intentionally excluded because they do not meet OmniCleaner's Windows 11 safety/value threshold.
