# Release Policy

This document describes the versioning and release process for the `labrats_work.modules_ansible` Ansible collection.

## Versioning

This collection follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html) (SemVer):

- **MAJOR** version for incompatible API changes
- **MINOR** version for new functionality in a backward compatible manner
- **PATCH** version for backward compatible bug fixes

### Version Format

```
MAJOR.MINOR.PATCH
```

Example: `1.2.3`

## Release Process

### Automated Releases

Releases are automated through GitHub Actions:

1. **Create a Pull Request** with your changes targeting `main` branch
2. **Merge the PR** after review/approval
3. **Automatic versioning** happens on merge:
   - A new git tag is created (patch version bump)
   - A PR is automatically created to update `galaxy.yml` and `CHANGELOG.md`
4. **Merge the version bump PR** to complete the release

### What Triggers a Release

- Every merged PR to `main` creates a new patch release
- Version bump PRs (prefixed with `chore: bump version`) do not trigger additional releases

### Manual Version Bumps

For minor or major version bumps, manually update the version before merging:

1. Update `galaxy.yml` with the new version
2. Update `CHANGELOG.md` with the new version section
3. Create and merge the PR
4. The workflow will create the tag for the version in `galaxy.yml`

## Changelog

All notable changes are documented in [CHANGELOG.md](CHANGELOG.md) following the [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) format.

### Changelog Categories

- **Added** - New features
- **Changed** - Changes in existing functionality
- **Deprecated** - Soon-to-be removed features
- **Removed** - Removed features
- **Fixed** - Bug fixes
- **Security** - Vulnerability fixes

## Deprecation Policy

1. Features are marked as **deprecated** in a minor release
2. Deprecated features are **removed** only in the next major release
3. Deprecation notices are documented in:
   - `CHANGELOG.md`
   - Role/module documentation
   - Ansible deprecation warnings (when applicable)

## Compatibility

### Ansible Version Support

- Minimum supported Ansible version is defined in `meta/runtime.yml`
- Currently: `requires_ansible: ">=2.14.0"`

### Breaking Changes

Breaking changes require a major version bump and must be:

1. Documented in `CHANGELOG.md` under **Changed** or **Removed**
2. Announced in the PR description
3. Include migration instructions when applicable

## Installing Specific Versions

```yaml
# requirements.yml
collections:
  - name: https://github.com/labrats-work/modules-ansible.git
    type: git
    version: 1.0.71  # Specific version
```

Or use version ranges:

```yaml
collections:
  - name: https://github.com/labrats-work/modules-ansible.git
    type: git
    version: ">=1.0.0,<2.0.0"  # Any 1.x version
```
