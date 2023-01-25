# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_labels

This role sets labels for Docker Swarm cluster nodes. It can be run on any node with Manager level. 

The `swarm_labels_hostname` parameter must contain the Docker Swarm hostname, which may not be the same as the DNS or 
local hostname! 

### Examples

```yaml
- ansible.builtin.include_role:
    name: "softing_swarm_labels"
  vars:
    swarm_labels_hostname: "hostname"
    swarm_labels_labels:
      - key: purpose
        value: apps
```

## License

[GNU GPLv3](../../LICENSE)
