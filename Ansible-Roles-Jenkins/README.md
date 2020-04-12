## Ansible role to install `jenkins`

Workflow: 
- It ensures that `wget` is installed
- installs `openjdk-1.8.0` by yum
- fetches the GPG key and verifies by rpm_key
- installs jenkins by dnf
- starts jenkins service by `systemd`
- enables it by `systemd`   

to execute the playbook : `ansible-playbook -K main.yml`

-k to provide sudo access.