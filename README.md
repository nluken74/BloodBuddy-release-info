# BloodBuddy Release Information

This public repository contains version metadata and reviewed release notes for
BloodBuddy. It contains no application source code, APKs, medical records, local
profile identifiers, database statistics, or publishing credentials.

## Public Feed

The latest stable metadata is available without authentication:

https://raw.githubusercontent.com/nluken74/BloodBuddy-release-info/main/latest.json

Each published version has metadata and notes under `releases/<tag>.json` and
`releases/<tag>.md`. Older release notes remain available when newer versions are
published.

## Schema Version 1

| Field | Meaning |
| --- | --- |
| `schemaVersion` | Feed contract version, currently `1`. |
| `version` | Stable numeric major/minor/patch app version. |
| `tag` | Matching source release tag with a leading `v`. |
| `commit` | Source commit used for that app release, not this metadata repository's commit. |
| `releaseNotesUrl` | Public version-specific release notes in this repository. |
| `releaseUrl` | Corresponding existing BloodBuddy release page. |

## Downloads and Privacy

[BloodBuddy's project repository](https://github.com/nluken74/BloodBuddy) and its
release downloads may require GitHub access. Publishing this metadata does not make
the source code or APKs public and does not provide an automatic installer.

The app's update check requires no developer token and does not send blood values or
local database statistics. Publisher credentials remain in the source repository's
GitHub Actions secrets, not in this repository or the app.

## Publication

The initial feed identifies the reviewed existing `v0.0.7` release. Subsequent stable
release publication updates versioned files and latest metadata atomically. Older
retries do not downgrade the latest stable version or remove other releases' notes.