# Changelog

All notable changes to this collection will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.74] - 2026-01-09

### Changed
- Fix Kubernetes GPG key to always refresh (#29)

## [1.0.72] - 2026-01-09

### Changed
- Fix YAML syntax in auto-version workflow (#24)

## [1.0.71] - 2026-01-09

### Added
- `meta/runtime.yml` specifying minimum Ansible version (>=2.14.0)
- `CHANGELOG.md` following Keep a Changelog format
- `RELEASING.md` documenting release policy
- Auto-versioning workflow that creates tags and PRs on merge to main

### Changed
- Updated `kubernetes_node` role default version to 1.32.0 (semantic versioning format)

## [1.0.70] - 2026-01-09

### Changed
- Simplified auto-versioning workflow to tag-only approach

## [1.0.69] - 2026-01-09

### Added
- Auto-versioning GitHub Actions workflow

## [1.0.68] - 2026-01-09

### Changed
- Updated `kubernetes_node` role to use semantic versioning format

## [1.0.67] - 2026-01-09

### Fixed
- Updated Kubernetes apt repository from deprecated `apt.kubernetes.io` to `pkgs.k8s.io`
- Added version extraction for Kubernetes repository URL construction

## [1.0.66] - 2026-01-09

### Fixed
- Updated Helm role repository from deprecated Balto CDN to Buildkite

## [1.0.65] - 2026-01-09

### Added
- LICENSE file
- CODE_OF_CONDUCT.md

## [1.0.64] and earlier

- Initial collection releases with roles for:
  - `containerd` - Container runtime installation
  - `docker` - Docker installation
  - `helm` - Helm package manager
  - `kubernetes_node` - Kubernetes node setup
  - `kubernetes_init` - Kubernetes cluster initialization
  - `calico_init` - Calico CNI setup
  - `fluxcd` - FluxCD GitOps installation
  - `systemd_haproxy` - HAProxy load balancer
  - `kvm_setup` - KVM hypervisor setup
  - `lvm_setup` - LVM storage configuration

[Unreleased]: https://github.com/labrats-work/modules-ansible/compare/1.0.74...HEAD
[1.0.71]: https://github.com/labrats-work/modules-ansible/compare/1.0.70...1.0.71
[1.0.70]: https://github.com/labrats-work/modules-ansible/compare/1.0.69...1.0.70
[1.0.69]: https://github.com/labrats-work/modules-ansible/compare/1.0.68...1.0.69
[1.0.68]: https://github.com/labrats-work/modules-ansible/compare/1.0.67...1.0.68
[1.0.67]: https://github.com/labrats-work/modules-ansible/compare/1.0.66...1.0.67
[1.0.66]: https://github.com/labrats-work/modules-ansible/compare/1.0.65...1.0.66
[1.0.65]: https://github.com/labrats-work/modules-ansible/releases/tag/1.0.65
[1.0.72]: https://github.com/labrats-work/modules-ansible/compare/1.0.71...1.0.72
[1.0.74]: https://github.com/labrats-work/modules-ansible/compare/1.0.73...1.0.74
