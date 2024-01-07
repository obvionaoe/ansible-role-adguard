Ansible Role: adguard
=========

This role configures an AdGuard Home instance using [Docker](https://docker.io) on Linux.

Requirements
------------

- [Docker](https://docker.io)

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
adguard_version: "latest"
```

The version of AdGuard Home.

```yaml
adguard_container_name: "adguard"
```

The Docker container name.

```yaml
adguard_config_dir: "/adguard/conf"
adguard_data_dir: "/adguard/work"
```

The directories for configuration and data files.

```yaml
adguard_dns_port: 53
adguard_http_port: 80
```

The ports to use for the instance.

```yaml
adguard_enable_dhcp: false
```

Controls if AdGuard Home should run as a DHCP server.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: obvionaoe.adguard
```

License
-------

MIT

Author Information
------------------

This role was created in 2024 by [Luís Guimarães](https://obvionaoe.dev).
