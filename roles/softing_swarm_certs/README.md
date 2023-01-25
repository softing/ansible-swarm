# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_certs

Certificate generator for Docker Swarm cluster nodes. Root certificates, certificates for the cluster nodes (Linux host) 
and for the client (Linux users) will be created in the /resources/swarm folder.

The certificates will include the ip addresses of the cluster nodes, and the specified domain names.

### Examples

```yaml

- ansible.builtin.include_role:
    name: "softing_swarm_certs"
    apply:
      become: false
      delegate_to: "localhost"
      run_once: true
  vars:
    swarm_certs_domain: "swarm.domain.com"
    swarm_certs_folder: "/resources/swarm"
    swarm_certs_nodes: 
      - ip: 10.0.0.1
        hostname: hostname1
        domain: domain.com
      - ip: 10.0.0.2
        hostname: hostname2
        domain: domain.com
```

## License

[GNU GPLv3](../../LICENSE)
