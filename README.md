# Keylime-Ansible

Ansible configuration files for Keylime

## Changes made to ansible.cfg

```
[ssh_connection]
ssh_args=-o ForwardAgent=yes
```

## To install keylime and its dependencies (for agent)

Change to root directory of this project.

```
ansible-playbook --tags keylime_agent playbooks/keylime_playbook.yml
```

## To start swtpm, tpm2-abrmd, and keylime_ima_emulator in background

```
ansible-playbook --tags start_swtpm playbooks/keylime_playbook.yml
```

## To start keylime_agent

```
ansible-playbook --tags start_agent playbooks/keylime_playbook.yml
```

## To stop swtpm, tpm2-abrmd, keylime_ima_emulator, and keylime_agent together

Stop everything with this command so that you can have a clean restart later.

```
ansible-playbook --tags stop_all playbooks/keylime_playbook.yml
```
