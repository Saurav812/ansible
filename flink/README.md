# ansible-flink
Ansible role to configure apache flink. This role depends on ansible galaxy role [andrewrothstein.flink](https://galaxy.ansible.com/andrewrothstein/flink/) for installation

# Inventory 

_Example:_

```ini
[vsgflnk:children]
vsgflnk-master
vsgflnk-slaves

[vsgflnk-master]
btest1.vsg.comcast.net #Flink job server

[vsgflnk-slaves]
btest2.vsg.comcast.net #Flink task server
btest3.vsg.comcast.net #Flink task server
```

# Playbook

_Example:_
```yaml
# File: vsg_flink.yml
# Ansible playbook to install apache-flink, configure and start cluster
- hosts: flink
  become: true
  roles:
    - vsg.ansible-flink
```
