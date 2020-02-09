Role Name
=========

cockpit

[![Build Status](https://travis-ci.org/cmihai-ansible/cockpit.svg?branch=master)](https://travis-ci.org/cmihai-ansible/cockpit)

Ansible Galaxy:
---------------

[https://galaxy.ansible.com/devops-toolbox.cockpit](https://galaxy.ansible.com/devops-toolbox.cockpit)

```bash
ansible-galaxy install devops-toolbox.cockpit
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```
cockpit_enable_service: true
cockpit_firewall_configure: true
cockpit_firewall_rules:
  - port: 9090
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install cockpit on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: cockpit is configured
      import_role:
        name: devops-toolbox.cockpit
      vars:
        cockpit_enable_service: true
        cockpit_firewall_configure: true
        cockpit_firewall_rules:
          - port: 9090
      tags: cockpit
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/devops-toolbox.)
