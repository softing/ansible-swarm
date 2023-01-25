# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_server

This role installs Docker TLS certificates for specified Linux host. The 'swarm_server_node_ip' parameter must point to 
the local ip address to which Docer Swarm will be connected.

### Examples

```yaml
- ansible.builtin.include_role:
    name: "softing_swarm_server"
  vars:
    swarm_server_node_ip: "10.0.0.1"
    swarm_server_hostname: "{{ hostname }}"
    swarm_server_ca_domain: "{{ domain }}"
    swarm_server_ca_folder: "/resources/swarm"
```

## License

[GNU GPLv3](../../LICENSE)
