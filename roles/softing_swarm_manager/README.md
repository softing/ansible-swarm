# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_manager

This role connects a Linux host to a Docker Swarm cluster as a manager. The `swarm_master_host` parameter must point to 
the master node.

### Examples

```yaml
- ansible.builtin.include_role:
    name: "softing_swarm_manager"
  vars:
    swarm_manager_token: "{{ manager_token }}"
    swarm_master_host: "10.0.0.1"
```

## License

[GNU GPLv3](../../LICENSE)
