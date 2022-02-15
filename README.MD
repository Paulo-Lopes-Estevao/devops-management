# **DevOps**, Management of infrastructure and aprovisionament of environment



#### ANSIBLE

[Install Ansible]([https://link](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html))

Obs: install module 

> `ansible-galaxy collection install community.general -f`

>`ansible-galaxy collection install community.docker -f`

### Environment preparation

#### - Docker
#### - jenkins
#### - Terraform


> $ `ansible -i ansible/hosts all -m ping`


When trying to connect to a host when it gives an error

```
host | UNREACHABLE! => {
    "changed": false,
    "msg": "Failed to connect to the host via ssh: user@host: Permission denied (publickey,password).",
    "unreachable": true
}

```

> we should copy our ssh key to the host
`ssh-copy-id user@host`



> for execution **remote** `ansible-playbook -i ansible/hosts ansible/ansible.yml -K`


> for execution **localhost** `ansible-playbook -i ansible/hosts ansible/ansible.yml --connection=local -K`


> for execution `ansible-playbook -i ansible/hosts ansible/ansible.yml --vault-password-file=`s


<br>

### DOCKER

> check **docker** installation `docker --help`

### TERRAFORM

> check **terraform** installation `terraform --help`

### JENKINS

> open the browser and access **jenkins**  `host:8086`