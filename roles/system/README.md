System
=========

Initial setup for hosts in my homelab.


Requirements
------------

Any Ubuntu/Debian host is compatible.

Role Variables
--------------

Available defaults are documented in [defaults/main.yml](./defaults/main.yml) file.
Available variables are documented in [vars/main.yml](./vars/main.yml) file.

> :warning: This role will apply system configurations you may not like, read it before executing.

> :warning: Changing the SSH port more than once, will fail. Make sure you set the right port before running the playbook.

> :warning: The role needs `gather_facts: no` in order to get correct ansible_port value. Facts will be gathered automatically after running ssh tasks.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  gather_facts: no
  vars:
    ansible_port: 2222
    timezone: "Europe/Rome"
  collections:
    - federicoantoniazzi.homelab
  roles:
    - system
```

License
-------

MIT

Author Information
------------------

This role was created in 2021 by [Federico Antoniazzi](https://www.federicoantoniazzi.dev).
