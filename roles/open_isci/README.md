# open_isci

Install and configure Open-iSCSI initiator for iSCSI storage connectivity.

## Requirements

None.

## Role Variables

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|
| `state` | No | `present` | Set to `absent` to uninstall |

## Example Playbook

```yaml
- hosts: storage_clients
  tasks:
    - name: Install Open-iSCSI
      ansible.builtin.import_role:
        name: labrats_work.modules_ansible.open_isci

    - name: Remove Open-iSCSI
      ansible.builtin.import_role:
        name: labrats_work.modules_ansible.open_isci
      vars:
        state: absent
```

## License

GPL-3.0-or-later
