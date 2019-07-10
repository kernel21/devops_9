deploy_docker_compose
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
_docker_packages:

_python_packages:


A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

deploy_docker.yml Playbook:
----------------

`ansible-playbook deploy_docker.yml --extra-var "DOCKERHOSTS=docker_host"`

    name: Deploy docker-composer
    hosts: "{{ DOCKERHOSTS }}"
    become: yes

     roles:
    - { role: deploy_docker_compose, when: ansible_system == 'Linux' }`

License
-------

GPL2+