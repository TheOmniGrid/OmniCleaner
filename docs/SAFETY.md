# Safety model

OmniCleaner treats cleanup as a planned system change, not a blind delete operation.

## Analyze → Review → Clean

1. **Analyze is read-only.** Selected rules produce candidates and metadata without applying cleanup actions.
2. **Review is explicit.** The UI exposes paths, sizes, sources, modified dates, risk labels, and intended behavior.
3. **Clean is confirmed.** OmniCleaner executes only a reviewed plan and revalidates its assumptions immediately before action.

## Execution safeguards

- Stable rule and candidate identities prevent unrelated results from being substituted into a plan.
- Candidate paths are normalized and revalidated before execution.
- Drive roots, Windows roots, user-profile roots, and other protected locations are blocked from unsafe recursive treatment.
- Reparse points are treated as boundaries to avoid crossing into unexpected trees.
- User exclusions apply to the selected folder and its descendants.
- Cleanup budgets can cap unattended runs.
- Supported active browsers can trigger review warnings.
- Advanced-risk rules are hidden from the default path until deliberately enabled.
- Scheduled runs can be analyze-only.
- Shortcut inspection never probes UNC or mapped-network targets, so a local review cannot initiate SMB authentication.
- Similar-photo inputs are capped at 64 MiB and 100 megapixels and use a bounded decode; DISM output is capped per stream.
- Contained Omni-suite applications require explicit selection and are not launched while OmniCleaner is elevated.

## Recovery choices

| Mode | Intended use |
|---|---|
| **Recycle Bin** | Recommended default for recoverable file cleanup. |
| **Quarantine** | Moves supported items into a managed local recovery area with retention controls. |
| **Permanent** | Available only as an explicit choice for users who understand the consequence. |

History and recovery records are stored locally. Quarantined items can be restored while retained.

## Duplicate safety

Duplicate candidates pass through progressively stronger checks: equal size, sample hash, full SHA-256, and final byte-for-byte comparison. OmniCleaner still requires explicit user selection; similarity is never treated as proof of dispensability.

## Empty-directory safety

Empty-directory scans are recursive and previewed. Protected roots and reparse points are excluded. Parent directories are reconsidered only after child processing, so the final action reflects current state rather than stale scan state.

## Definitions, native tools, and elevation

Imported definitions are data, not executable extensions: commands, scripts, installers, registry deletion, and automatic enablement are rejected. Signed online or offline catalogues prove publisher control but still import rules disabled for review. Windows maintenance actions use supported native surfaces where appropriate. OmniCleaner does not auto-elevate, and it refuses to use an elevated process to launch sibling Omni applications.

## Intentional non-features

OmniCleaner does not provide:

- A bulk registry cleaner.
- Automatic driver replacement.
- Forced shutdown of browsers or other applications.
- Unattended application uninstallers.
- RAM “boosting” or fabricated speed scoring.
- Multi-pass SSD secure-wipe claims.
- Aggressive service-disable presets.

These operations have poor or unpredictable risk/reward on modern Windows 11 systems. When Windows already provides an appropriate native surface, OmniCleaner opens or inventories that surface instead.

## A necessary reminder

No maintenance tool can make every third-party application state predictable. Review the plan, keep normal backups, use Recycle Bin or quarantine for important systems, and avoid cleaning while applications are actively writing data.
