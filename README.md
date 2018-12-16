Ansible Role Grafana
=========

[![Build Status](https://travis-ci.org/orachide/ansible-role-grafana.svg?branch=master)](https://travis-ci.org/orachide/ansible-role-grafana)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-orachide-660198.svg)](https://galaxy.ansible.com/orachide)

Ansible role that install Grafana with provisioning datasources and dashboards.

Requirements
------------

This version work only on `CentOS`

Role Variables
--------------

A description of the settable variables for this role should go here, including
any variables that are in defaults/main.yml, vars/main.yml, and any variables
that can/should be set via parameters to the role. Any variables that are read
from other roles and/or the global scope (ie. hostvars, group vars, etc.) should
be mentioned here as well.

Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```json
---
- name: Converge
  hosts: all
  roles:
    - role: ansible-role-grafana
      grafana_install_root_folder: /opt/grafana
      grafana_data_dir: "{{ grafana_install_root_folder }}"
      grafana_home_dir: "{{ grafana_install_root_folder }}"
      grafana_datasources_templates_path: "{{ playbook_dir }}/templates/datasources"
      grafana_dashboards_templates_path: "{{ playbook_dir }}/templates/dashboards"
      grafana_dashboards_config_template: "{{ playbook_dir }}/templates/dashboards-config.yml.j2"

```

License
-------

BSD

Author Information
------------------

This role was created in 2018 by [Rachide Ouattara](https://orachide.chidix.fr/).
