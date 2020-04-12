This role adds a new user to your localhost machine, you can change that by changing it in the main playbook `hosts:<MyHost>`

it adds the user with name `codein` with uid `1040`

To execute `ansible-playbook -K main.yml`

`-k` to provide sudo access to the playbook. 