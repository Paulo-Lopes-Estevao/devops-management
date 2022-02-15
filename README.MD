# Using Ansible for Management of infrastructure and aprovisionament of environment



#### ANSIBLE

### [Install Ansible]([https://link](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html))

> `ansible-galaxy collection install community.general -f`

>`ansible-galaxy collection install community.docker -f`

### Preparação do ambiente


## - Docker
## - Terraform


> $ `ansible -i ansible/hosts all -m ping`


Ao tentar se conectar com um host quando der erro

```
host | UNREACHABLE! => {
    "changed": false,
    "msg": "Failed to connect to the host via ssh: user@host: Permission denied (publickey,password).",
    "unreachable": true
}

```

> devemos copiar a nossa chave ssh para o host
`ssh-copy-id user@host`



> para execução **remote** `ansible-playbook -i ansible/hosts ansible/ansible.yml -K`


> para execução **localhost** `ansible-playbook -i ansible/hosts ansible/ansible.yml --connection=local -K`


> para execução `ansible-playbook -i ansible/hosts ansible/ansible.yml --vault-password-file=`s