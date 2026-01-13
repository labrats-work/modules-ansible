# kubernetes_node

> **DEPRECATED**: This role has been moved to [labrats.work.hetzner.cluster](https://github.com/labrats-work/labrats.work.hetzner.cluster/tree/main/ansible/roles/kubernetes_node) for faster iteration on Kubernetes-specific changes.

Installs Kubernetes node components (kubelet, kubeadm, kubectl).

## Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `kubernetesVersion` | required | Kubernetes version (e.g., "1.35.0") |

## Migration

For new deployments, copy this role to your project's `ansible/roles/` directory and use it locally. This eliminates the modules-ansible release cycle overhead.
