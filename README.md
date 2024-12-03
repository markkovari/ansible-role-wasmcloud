# wasmCloud Ansible Role


[![ci](https://github.com/markkovari/ansible-role-wasmcloud/actions/workflows/ci.yaml/badge.svg)](https://github.com/markkovari/ansible-role-wasmcloud/actions/workflows/ci.yaml)

wasmCloud is a secure, portable, and lightweight WebAssembly host runtime for building cloud-native applications. This Ansible role will deploy a wasmCloud host runtime on your servers.

## Installation

```yaml
# requirments.yaml
- src: git@github.com:markkovari/ansible-role-wasmcloud.git
  scm: git
  version: main
  name: wasmcloud
```

## Role Variables

[see default variables](defaults/main.yaml)

## Example Playbook

```yaml
- hosts: some_servers
  roles:
    - wasmcloud
```
