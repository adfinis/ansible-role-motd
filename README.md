# [motd](#motd)

Configure `/etc/issue` and `/etc/motd` with Ansible.

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](./molecule/default/converge.yml).

```yaml
---
- name: Converge
  hosts: all
  become: yes  # `no` will also work.

  roles:
    - role: adfinis.motd
```

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](./defaults/main.yml):

```yaml
---

# MOTD message (``/etc/motd``).
motd_message: |
  -------------------------------------------------
          This system is managed by Ansible
  -------------------------------------------------

# Issue message (``/etc/issue`` and ``/etc/issue.net``).
motd_issue_message: |
  -------------------------------------------------
          This system is managed by Ansible
  -------------------------------------------------

# If to install and use cowsay in the motd messages
motd_cowsay: false
```

## [Requirements](#requirements)

- None

## [Compatibility](#compatibility)

This role is only compatible with debian bullseye and bookworm.

The minimum version of Ansible required is 2.12.

## [License](#license)

`GPL-3.0 <https://github.com/adfinis-sygroup/ansible-role-motd/blob/master/LICENSE>`_

## [Author Information](#author-information)

motd role was written by:

* Adfinis AG | `Website <https://www.adfinis.com/>`_ | `Twitter <https://twitter.com/adfinis>`_ | `GitHub <https://github.com/adfinis>`_
