# labrats_work.modules_ansible

Ansible collection with reusable roles for infrastructure automation.

## Requirements

- Ansible >= 2.14.0

## Installation

```yaml
# requirements.yml
collections:
  - name: https://github.com/labrats-work/modules-ansible.git
    type: git
    version: 1.0.71
```

```bash
ansible-galaxy collection install -r requirements.yml
```

## Included Roles

| Role | Description |
|------|-------------|
| `containerd` | Container runtime installation |
| `docker` | Docker installation and configuration |
| `helm` | Helm package manager |
| `kubernetes_node` | Kubernetes node prerequisites (kubelet, kubeadm, kubectl) |
| `kubernetes_init` | Kubernetes cluster initialization with kubeadm |
| `calico_init` | Calico CNI setup |
| `fluxcd` | FluxCD GitOps installation |
| `systemd_haproxy` | HAProxy load balancer |
| `systemd_node_exporter` | Prometheus node exporter |
| `kvm_setup` | KVM hypervisor setup |
| `lvm_setup` | LVM storage configuration |

## Usage

```yaml
- hosts: kubernetes_nodes
  tasks:
    - name: Install Kubernetes prerequisites
      ansible.builtin.import_role:
        name: labrats_work.modules_ansible.kubernetes_node
      vars:
        kubernetesVersion: "1.32.0"
```

## Documentation

- [CHANGELOG.md](CHANGELOG.md) - Version history and changes
- [RELEASING.md](RELEASING.md) - Versioning and release policy
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - Community guidelines

## License

GPL-3.0-or-later
