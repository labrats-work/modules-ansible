# fluxcd

Install and configure FluxCD for GitOps continuous deployment.

## Requirements

- Kubernetes cluster with kubectl configured
- GitHub personal access token with repo permissions

## Role Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `flux_init_owner` | Yes | GitHub owner/organization for FluxCD repository |
| `flux_init_repo` | Yes | GitHub repository name for FluxCD configuration |
| `flux_init_path` | Yes | Path within the repository for cluster configuration |
| `flux_init_token` | Yes | GitHub personal access token |

## Example Playbook

```yaml
- hosts: kubernetes_master
  tasks:
    - name: Bootstrap FluxCD
      ansible.builtin.import_role:
        name: labrats_work.modules_ansible.fluxcd
      vars:
        flux_init_owner: my-org
        flux_init_repo: my-cluster-flux
        flux_init_path: clusters/production
        flux_init_token: "{{ github_token }}"
```

## License

GPL-3.0-or-later
