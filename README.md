# Ansible Role wasmCloud

> [!CAUTION]
> This role is still in development and not yet ready for production use yet.
> It probably will work for some use cases, but some of them are lacking or not yet implemented.

Feel free to open an issue or a pull request if you have any suggestions or improvements.

[![ci](https://github.com/markkovari/ansible-role-wasmcloud/actions/workflows/ci.yaml/badge.svg)](https://github.com/markkovari/ansible-role-wasmcloud/actions/workflows/ci.yaml)

wasmCloud is a secure, portable, and lightweight WebAssembly host runtime for building cloud-native applications. This Ansible role will deploy a wasmCloud host runtime on your servers.

> [!INFO]
> Currently creating the credentials file is manual and requires a bit of modification to the file. This _might_ be automated in the future.

## Creds file creation steps

1. install the [nsc tool](https://docs.nats.io/using-nats/nats-tools/nsc)
1. create a new operator account
```console
nsc add operator {{MyOperator}}
```
1. Find the operator account in the `~/.nkeys/{{MyOperator}}/` directory
1. Copy the `{{MyOperator}}.creds` file to the roo tof this folder and rename it as the `nats_credentials_file_path_source`

Be careful not to commit the file, it contains sensitive information.
Use gitignore/ansible-vault/sops to protect the file.

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
