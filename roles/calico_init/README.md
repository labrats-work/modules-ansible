# calico_init

> **DEPRECATED**: This role has been moved to [labrats.work.hetzner.cluster](https://github.com/labrats-work/labrats.work.hetzner.cluster/tree/main/ansible/roles/calico_init) for faster iteration on Kubernetes-specific changes.

Installs Calico CNI via the Tigera operator.

## Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `calico_version` | `v3.31.2` | Calico version to install |
| `yaml_configs` | required | List of Installation/APIServer CRDs |

## Migration

For new deployments, copy this role to your project's `ansible/roles/` directory and use it locally. This eliminates the modules-ansible release cycle overhead.
