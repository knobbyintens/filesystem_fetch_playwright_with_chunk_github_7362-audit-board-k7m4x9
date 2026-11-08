# Release Mirror Licensing Policy

This policy governs the mirror identifiers that may be quoted to downstream
partners for datasets listed in `catalog/datasets.json`.

Resolve the mirror identifier for a dataset as follows:

1. If the dataset's `release_channel` is `internal`, the mirror identifier is
   `not-for-release`.
2. Otherwise, look up the dataset's `license_code` in
   `registry/license-registry.json`.
3. If the license `class` is `copyleft` and the dataset's `release_channel` is
   `partner`, the mirror identifier is `no-redistribution`.
4. Otherwise, the mirror identifier is the license's `spdx` value.

Never quote a license identifier that differs from the resolution above. The
registry is the only source of SPDX identifiers.

## Release channels

- `public`: datasets published on the public hub.
- `partner`: datasets mirrored privately for approved partners.
- `internal`: datasets that may not leave the organization.
