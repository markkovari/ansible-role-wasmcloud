# Ansible Role wasmCloud


> [!CAUTION]
> This role is still in development and not yet ready for production use yet.
> It probably will work for some use cases, but some of them are lacking or not yet implemented.

Feel free to open an issue or a pull request if you have any suggestions or improvements.


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
