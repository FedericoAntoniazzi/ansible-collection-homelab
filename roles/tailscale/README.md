Role Name
=========

This role install tailscale with default settings.

Requirements
------------

None.

Role Variables
--------------

Available defaults are documented in [defaults/main.yml](./defaults/main.yml) file.
Available variables are documented in [vars/main.yml](./vars/main.yml) file.

> :warning: The role requires `tailscale_auth_key` variable to be set, otherwise will exit without doing nothing.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  gather_facts: yes
  vars:
    tailscale_auth_key: "tskey-"
  collections:
    - federicoantoniazzi.homelab
  roles:
    - tailscale
```

License
-------

BSD

Author Information
------------------

This role was created in 2022 by [Federico Antoniazzi](https://www.federicoantoniazzi.dev).
