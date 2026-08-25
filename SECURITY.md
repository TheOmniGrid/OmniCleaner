# Security policy

## Supported version

Security fixes currently target the latest released OmniCleaner 1.x build.

## Reporting a vulnerability

Please use GitHub’s **Report a vulnerability** option on this repository’s Security tab. This creates a private report visible to the repository maintainers.

Include:

- OmniCleaner version and Windows architecture.
- A concise description of the impact.
- Reproduction steps or a minimal proof of concept.
- Whether cleanup execution, path validation, catalogs, quarantine, or elevation is involved.
- Any suggested mitigation.

Do not include secrets, personal data, or destructive payloads. Please allow reasonable time for validation and remediation before public disclosure.

## Scope priorities

Reports involving path-boundary bypasses, reparse-point behavior, cleanup-plan substitution, catalog signature validation, quarantine restoration, privilege boundaries, or unintended network activity are especially important.

## 1.0.0 security posture

- Cleanup plans bind candidate metadata and are revalidated before execution; protected roots, exclusions, UNC paths, and reparse boundaries are enforced at analysis and execution time.
- Recycle Bin is the default. Quarantine uses contained identities, integrity metadata, retention state, and collision-safe restoration; permanent actions require explicit confirmation.
- Imported rules cannot execute commands, PowerShell, installers, registry deletion, or forced process termination. Signed catalogue imports still begin disabled and are not eligible for unattended automation.
- Core cleanup is offline. Network-capable catalogue/update checks require explicit user action, public HTTPS, byte limits, redirect/private-address validation, SHA-256 where applicable, and RSA-PSS signatures. Application updates are never downloaded or installed automatically.
- Shortcut Health never probes UNC or mapped-network targets, preventing analysis-driven SMB authentication. Contained Omni-suite programs are not launched while OmniCleaner is elevated.
- Similar-photo review rejects inputs above 64 MiB or 100 megapixels and uses a bounded decode; DISM analysis output is bounded to 4 MiB per stream.
- A standard 1.0.0 security scan's single medium UNC-authentication finding was remediated and regression-tested. No critical, high, or medium finding remains open.

Remaining defense-in-depth work includes binding destination validation to the connected catalogue transport, hostile-image codec fuzzing, and handle-bound file mutation before any future elevated cleanup mode. These limits are documented and do not weaken the non-elevated, preview-first default.
