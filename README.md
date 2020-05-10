Gold Config
=========

Demonstration ansible Role to check and enforce a golden configuration to Cisco network gear.

Requirements
------------

N/A

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Variable File
------------
```
ansible_connection: network_cli
ansible_user: "{{username}}"
ansible_ssh_pass: "{{password}}"
ansible_network_os: nxos

checkmode: yes

domain_name: virl.info 
domain_search: "{{domain_name}}"

ntp_servers: 
  - 8.8.8.8
  - 10.1.1.1
log_servers:
  - 10.1.1.1
  - 10.1.1.2

features:
  - nxapi
  - restconf
  - netconf

```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- name: Check if devices match the Gold config
  hosts: lab
  gather_facts: no

  roles: 
    - gold_config


License
-------

CISCO SAMPLE CODE LICENSE

Author Information
------------------

Eric D. Thiel 
