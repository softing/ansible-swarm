# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_client

This role installs Docker TLS certificates for specified users.

### Examples

```yaml
- ansible.builtin.include_role:
    name: "softing_swarm_client"
  vars:
    swarm_client_hostname: "{{ hostname }}"
    swarm_client_ca_domain: "{{ domain }}"
    swarm_client_ca_folder: "/resources/swarm"
    swarm_client_docker_users:
      - user: root
        folder: /root
      - user: docker
        folder: /home/docker
```

## License

[GNU GPLv3](../../LICENSE)
