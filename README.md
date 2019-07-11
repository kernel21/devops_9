deploy_docker_compose
=========

Deploy docker container by docker-compose

Requirements
------------

OS: Ubuntu 16.04

Role Variables
--------------

vars/main.yml:

__docker_packages
_python_packages_

defaults/main.yml:

_project_folder: /tmp/compose/
project_name: lab7ms_ansible
service_name: servlets_

deploy_docker.yml:

_hosts: "{{ DOCKERHOSTS }}"_

deploy_docker.yml Playbook:
----------------


`ansible-playbook deploy_docker.yml --extra-var "DOCKERHOSTS=docker_host ansible_python_interpreter=/usr/bin/python3"`

    name: Deploy docker-composer
    hosts: "{{ DOCKERHOSTS }}"
    become: yes

     roles:
    - { role: deploy_docker_compose, when: ansible_system == 'Linux' }`

License
-------

GPL2+