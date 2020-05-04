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
siteid: 19
tenants:
  - tenant_name: finance
    tenant_num: 11
    segments:
      - vlan_num: 1
        name: "{{siteid}}-finance-data"
        subnet: "10.{{siteid}}.111.0/24"
      - vlan_num: 2
        name: "{{siteid}}-finance-voice"
        subnet: "10.{{siteid}}.112.0/24"
  - tenant_name: engineering
    tenant_num: 12
    segments:
      - vlan_num: 1
        name: "{{siteid}}-engineering-data"
        subnet: "10.{{siteid}}.121.0/24"
      - vlan_num: 2
        name: "{{siteid}}-engineering-voice"
        subnet: "10.{{siteid}}.122.0/24"
  - tenant_name: hr
    tenant_num: 13
    segments:
      - vlan_num: 1
        name: "{{siteid}}-hr-data"
        subnet: "10.{{siteid}}.131.0/24"
      - vlan_num: 2
        name: "{{siteid}}-hr-voice"
        subnet: "10.{{siteid}}.132.0/24"
  - tenant_name: facilities
    tenant_num: 14
    segments:
      - vlan_num: 1
        name: "{{siteid}}-facilities-data"
        subnet: "10.{{siteid}}.141.0/24"
      - vlan_num: 2
        name: "{{siteid}}-facilities-voice"
        subnet: "10.{{siteid}}.142.0/24"
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- name: Use roles to create VRFs
  hosts: nx
  gather_facts: false

  roles:
    - network-vrf


License
-------

CISCO SAMPLE CODE LICENSE

Author Information
------------------

Eric D. Thiel 
