# Ansible Role: CTFd ([Ludus](https://ludus.cloud))

An Ansible Role that will deploy the CTFd application via Docker

## Requirements

- community.docker

## Role Variables

None.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: hosts
  roles:
    - PrymalInstynct.ludus_ctfd
```

## Example Ludus Range Config

```yaml
ludus:
  - vm_name: "{{ range_id }}-ctfd"
    hostname: "{{ range_id }}-ctfd"
    template: debian-12-x64-server-template
    vlan: 10
    ip_last_octet: 1
    ram_gb: 4
    cpus: 2
    linux: true
    roles:
      - PrymalInstynct.ludus_ctfd
```

## License

GPLv3

## Author Information

This role was created by [PrymalInstynct](https://github.com/PrymalInstynct), for [Ludus](https://ludus.cloud/).
