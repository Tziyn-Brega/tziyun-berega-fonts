# Tziyun Berega — font pack

The downloadable fonts for **ציון ברגע** (Tziyun Berega). The app ships a small
core set inside its installer and installs the rest from the **latest release**
of this repository, one archive per font family.

## What a release contains

- `pack-manifest.json` (+ `pack-manifest.json.sha256`) — every family, its
  archive, and every file in it with its exact name, size and sha256.
- `<family>.zip` — that family's font files.

The app installs a family only when the archive matches the manifest's sha256
and every file in it is byte-for-byte a file the manifest lists, with the listed
size and sha256; names are checked against one set of rules on every OS (UTF-8,
NFC, no path separators, no Windows device names). A family installs all or
nothing. The same pack can be installed offline from a folder.

Releases are built and published by `verify-legal-fonts` (`fontpack export`),
which runs the app's own install check over the pack before publishing.

## Licences

Every font here is redistributed under its own licence — see
[LICENSES.md](LICENSES.md) and [`licenses/`](licenses/).
