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
