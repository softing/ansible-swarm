# Sofing • Ansible • Docker Swarm

**Different Ansible roles for for working in a Docker Swarm environment**

```
01010011 01001111 01000110 01010100 01001001 01001110 01000111 
```

## About

### softing_swarm_service

Creating a Service to Run on a Docker Swarm Cluster. 

The `swarm_service_root` parameter is responsible for the base folder in which the service folder will be created and is 
`/srv` by default.

This role exports the 'swarm_service_path' fact which can be used to further customize the service.

The service will be started automatically after the Playbook is executed. Therefore, you can create files and perform 
other operations with service in Playbook.

### Examples

```yaml
- name: "Create Minio service"
  ansible.builtin.include_role:
    name: softing_swarm_service
  vars:
    swarm_service_name: minio
    swarm_service_root: /data/shared/services

- name: "Copy haproxy.cfg file"
  template:
    src: "haproxy.cfg"
    dest: "/{{ swarm_service_path }}/haproxy.cfg"
```

## License

[GNU GPLv3](../../LICENSE)
