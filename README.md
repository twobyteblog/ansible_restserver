# Ansible Role: Restic Rest Server

Ansible role which installs Restic's REST-based backup service for hosting backup repositories.

# Requirements

This role requires root access to the host system. Specify it globally, or add it to your playbook (example below).

```
- hosts: restserver
  roles:
    - role: ansible_restserver
      become: yes
```

# Installation

To use this role, clone the respository into the directory containing your other Ansible roles.

```
git clone https://github.com/inundationca/ansible_restserver.git
```

Add it to a new or existing playbook.

```
- hosts: backup_hosts
  roles:
    - role: ansible_restserver
      become: yes
```

Within your host or group variables, specify where your repositories will be stored.

```
restserver_backup_path: /opt/backups
```

