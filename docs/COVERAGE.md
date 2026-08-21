# Coverage and modernization

OmniCleaner was designed after studying the capabilities users value in CCleaner, BleachBit, CleanmgrPlus, FluentCleaner, Remove Empty Directories, and RED-style empty-directory tools. It is not a code fork or repackaging of those products. It is a distinct Windows 11 application with a conservative safety model.

## Capability coverage

| Tool category | What users expect | OmniCleaner coverage and improvement |
|---|---|---|
| General-purpose cleanup | Windows, browser, and application cleanup | 112 curated rules, risk classes, exact previews, exclusions, profiles, history, and recovery-first deletion modes. |
| Privacy cleanup | Recent traces and browser artifacts | Explicit privacy profile, per-rule descriptions, running-browser guidance, and no telemetry of its own. |
| Windows cleanup front ends | Access to native Windows maintenance | Windows-native inventory and handoffs, with unsupported or risky operations kept out of one-click presets. |
| Empty-directory tools | Recursive discovery and removal | Recursive preview, protected roots, reparse-point boundaries, configurable behavior, and parent revalidation. |
| Duplicate finders | Reliable duplicate identification | Size grouping, sample screening, full SHA-256, and final byte comparison before selection. |
| Storage analyzers | Explain where space is used | Folder and extension summaries, large files, trends, and cloud-placeholder-aware analysis. |
| App maintenance | Installed programs and startup control | Native uninstall handoff, reversible startup controls, service/task visibility, updates, and driver inventory. |
| Scheduling | Automatic maintenance | Windows Task Scheduler, profiles, analyze-only runs, budgets, shutdown options, and no resident service. |
| Extensible cleaners | Community or custom definitions | Winapp-style import, native schema, Rule Lab, and signed-catalog infrastructure. |

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
