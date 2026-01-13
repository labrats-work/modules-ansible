# kubernetes_init

> **DEPRECATED**: This role has been moved to [labrats.work.hetzner.cluster](https://github.com/labrats-work/labrats.work.hetzner.cluster/tree/main/ansible/roles/kubernetes_init) for faster iteration on Kubernetes-specific changes.

Orchestrates kubeadm init and join operations.

## Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `kubeadm` | required | Either `init` or `join` |
| `yaml_configs` | required | List of kubeadm configuration objects |

## Migration

For new deployments, copy this role to your project's `ansible/roles/` directory and use it locally. This eliminates the modules-ansible release cycle overhead.
