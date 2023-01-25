# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_initialize

This role runs the initialization of the Docker Swarm cluster and creates the master node. The `swarm_master_ip` 
parameter points to the address where Docker Swarm will run. This address will be used for Swarm communication. It 
should not be publicly available.

### Examples

```yaml
- ansible.builtin.include_role:
    name: "softing_swarm_initialize"
    public: yes
  vars:
    swarm_master_ip: "10.0.0.1"
```

## License

[GNU GPLv3](../../LICENSE)
