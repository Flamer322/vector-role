# Vector Ansible Role

An Ansible role for installing and configuring
[Vector](https://vector.dev/).

## Requirements

- Ansible >= 2.12
- Ubuntu 24.04
- Internet access to download Vector packages

## Role Variables

| Variable | Default | Description |
| --- | --- | --- |
| `vector_version` | `0.44.0` | Vector version |
| `vector_package_architecture` | `amd64` | Package architecture |
| `vector_deb_url` | Vector package URL | Download URL |
| `vector_config_path` | `/etc/vector/vector.yaml` | Configuration file path |
| `vector_service_enabled` | `true` | Enable service at boot |
| `vector_service_state` | `started` | Desired service state |

## Example Playbook

```yaml
---
- name: Install Vector
  hosts: vector
  become: true
  roles:
    - vector
