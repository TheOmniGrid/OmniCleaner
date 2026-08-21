# Privacy

OmniCleaner is designed as a local-first Windows utility.

## What OmniCleaner does not contain

- No telemetry or analytics.
- No advertising or offer bundles.
- No account or sign-in requirement.
- No cloud dashboard or cloud storage.
- No resident background service or tray process.
- No unsolicited update check.

## Local data

Settings, exclusions, history, storage snapshots, catalog metadata, and quarantine records are stored on the local computer under OmniCleaner’s application-data location. They are used to provide the requested functionality and are not uploaded by the application.

## Network access

Core cleaning, storage analysis, duplicate discovery, empty-directory discovery, app inventory, history, and recovery do not require network access.

Network access can occur only when the user explicitly requests a network-backed operation, such as:

- A WinGet/package update query or handoff.
- Retrieval of an explicitly configured HTTPS rule catalog.

Remote catalogs must pass configured digest and signature checks before definitions are accepted. OmniCleaner does not silently poll a catalog or application-update service.

## Public support services

The Patreon, Ko-fi, GitHub, and badge links in this documentation are external web services. Visiting those links is separate from running OmniCleaner and is governed by each service’s privacy policy.
