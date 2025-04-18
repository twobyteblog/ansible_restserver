## Ansible Role: Restic Rest Server

Ansible role to install [Restic's REST Server](https://github.com/restic/rest-server) for hosting backup repositories.

## Prerequisites

- Debian 11 or above.
- UFW firewall.

## Actions Performed

The role performs the following actions:

1. Install prerequisite packages.
2. Install Restic rest-server.
3. Open port 8000/tcp to allow remote connections to Rest Service.

## Setup Instructions

### Clone Repository

Clone the project into the roles directory of your Ansible Controller.

```bash
git clone https://github.com/twobyteblog/ansible_restserver.git
```

### Variables

Within your host or group variables, specify where your repositories will be stored.

```bash
restserver_backup_path: /opt/backups
```

### Playbooks

Create a playbook which runs this role. This role requires ```become``` privileges.

```bash
- hosts: restserver
  roles:
    - role: ansible_restserver
      become: yes
```

