# Coverage and modernization

OmniCleaner was designed after studying the capabilities users value in CCleaner, BleachBit, CleanmgrPlus, FluentCleaner, Remove Empty Directories, and RED-style empty-directory tools. It is not a code fork or repackaging of those products. It is a distinct Windows 11 application with a conservative safety model.

## Capability coverage

| Tool category | What users expect | OmniCleaner coverage and improvement |
|---|---|---|
| General-purpose cleanup | Windows, browser, and application cleanup | 112 curated rules, risk classes, exact previews, exclusions, profiles, history, and recovery-first deletion modes. |
| Privacy cleanup | Recent traces and browser artifacts | Explicit privacy profile, per-rule descriptions, running-browser guidance, and no telemetry of its own. |
| Windows cleanup front ends | Access to native Windows maintenance | Windows-native inventory and handoffs plus bounded supported DISM analysis, with unsupported or risky operations kept out of one-click presets. |
| Empty-directory tools | Recursive discovery and removal | Recursive preview, protected roots, reparse-point boundaries, configurable behavior, and parent revalidation. |
| Duplicate finders | Reliable duplicate identification | Size grouping, sample screening, full SHA-256, and final byte comparison before selection. |
| Storage analyzers | Explain where space is used | Folder/extension/treemap summaries, reusable scan sets, logical/on-disk and hard-link-aware totals, large files, trends, cloud state without hydration, and bounded local similar-photo review. |
| App maintenance | Installed programs and startup control | Native uninstall handoff, reversible startup controls, service/task visibility, updates, and driver inventory. |
| Scheduling | Automatic maintenance | Windows Task Scheduler, profiles, analyze-only runs, budgets, shutdown options, and no resident service. |
| Extensible cleaners | Community or custom definitions | Winapp-style import, native schema, Rule Lab, and signed-catalog infrastructure. |
| Windows 11 care tools | Low-space, update, downloads, shortcuts, and diagnostics guidance | Update/reboot/rollback readiness, ranked Low Storage Rescue, conservative Downloads review, no-probe shortcut health, Component Store insights, path-free diagnostics, and reversible Explorer integration. |

## Improvements over traditional cleanup patterns

### From “one click” to an inspectable plan

OmniCleaner separates read-only analysis from execution. Results remain selectable at item level and are revalidated before action. This reduces the risk of cleaning paths that changed between scanning and confirmation.

### Recovery before permanence

Recycle Bin is the default deletion mode. Quarantine and restoration are available where appropriate. Permanent deletion is a deliberate choice, not a marketing shortcut.

### Modern Windows boundaries

The scanners account for protected roots, directory reparse points, and cloud placeholders. The app avoids legacy claims—such as registry cleaning or RAM boosting—that are difficult to justify on current Windows systems.

### No resident “optimizer”

Automation uses Windows Task Scheduler. Closing OmniCleaner closes OmniCleaner: there is no tray process, background health watcher, service, ad component, or analytics process left running.

### Useful inventory without unsafe automation

OmniCleaner exposes installed apps, startup items, services, tasks, updates, packages, and drivers, but does not automatically remove applications, replace drivers, or disable arbitrary services.

### Hardened local inspection

Shortcut Health does not probe UNC or mapped-network targets, preventing a local review from initiating SMB authentication. Similar-photo inputs and decoder dimensions are bounded, DISM output is bounded, and contained Omni-suite tools are not launched from an elevated OmniCleaner process.

## 1.0.0 assurance status

- 49/49 deterministic Core tests, both WPF smoke targets, and CLI gates pass.
- The complete x64 installation/uninstallation lifecycle passes; x64 and ARM64 packages, portable archives, hashes, versions, and architecture were verified.
- The final security review has no open critical, high, or medium finding. Authenticode, physical ARM64 execution, broader fresh-VM/accessibility review, ETW measurements, DNS transport binding, and hostile-image codec testing remain documented assurance work.

## Deliberate limits

Some competitor features are intentionally not reproduced:

- Registry cleaning.
- Automated driver installation.
- Forced termination of active applications.
- Unattended third-party uninstall sequences.
- Multi-pass overwrite claims on SSDs.
- Synthetic health or speed scores.
- Always-running monitoring, tracking, or offer components.

These exclusions are product decisions: OmniCleaner prioritizes explainable value, native Windows capabilities, and recoverability.
