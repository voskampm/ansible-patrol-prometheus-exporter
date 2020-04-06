Role Name
=========

Ansible role to install the ORD_PAT_PROM_EXPORT KM on Unix and Linux Patrol agents.

Requirements
------------

BMC Patrol should be installed using Ordina work instructions. The role does not overwrite files used by othe KM's. A restart of the Patrol agent should not be nessecary unless the role is used to update the ORD_PAT_PROM_EXPORT KM. The role does not restart the Patrol agent. That is the responsibility of the admin using the role!


Role Variables
--------------
```
patrol_user: "patrol"
patrol_group: "root"

patrol_directory: "/opt/bmc/Patrol3"
patrol_psl_directory: "/opt/bmc/Patrol3/lib/psl"
patrol_knowledge_directory: "/opt/bmc/Patrol3/lib/knowledge"
```

Dependencies
------------

None

Example Playbook
----------------
```
---

- hosts: all
  become: yes
  tasks:
 
    - include_role:    
        name: ansible-patrol-prometheus-exporter
```

License
-------

Michiel Voskamp, Ordina, 2020


Author Information
------------------

Michiel Voskamp.
