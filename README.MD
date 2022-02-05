# INFRAESTRUTURA SNIR


# ANSIBLE

### Preparação do ambiente

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



> para execução `ansible-playbook -i ansible/hosts docker/tasks/main.yml -u docker -K`




> para execução `ansible-playbook -i ansible/hosts docker/tasks/main.yml -u docker --vault-password-file=`s