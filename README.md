# Keylime-Ansible

Ansible configuration files for Keylime

## Changes made to ansible.cfg

'''
[ssh_connection]
ssh_args=-o ForwardAgent=yes
'''

## inventory variables

'''
ansible_python_interpreter=/usr/bin/python3
'''

## To run the keylime playbook

'''
ansible-playbook ./playbooks/keylime_playbook.yml
'''
