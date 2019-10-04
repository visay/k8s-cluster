K8S Infrastructure Setup
------------------------

Tested with Ubuntu server 18.04 but that should be working with other Linux distro
with small adjustments.

Preparation
===========

- Setup 5 different Ubuntu servers
- Create a Linux user with sudo access without asking for password
- Update `remote_user = ubuntu` in `ansible.cfg` to your Linux user created above
- Configure DNS or update /etc/hosts file

```
# Kubernetes
10.10.10.10 k8s-master
10.10.10.11 k8s-node-1
10.10.10.12 k8s-node-2
10.10.10.13 k8s-node-3
10.10.10.14 k8s-node-4
```

Provision the cluster
=====================

```
ansible-playbook playbook.yml
```

Reset the cluster
=================

```
ansible-playbook reset.yml
```
