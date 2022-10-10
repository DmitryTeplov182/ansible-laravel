## Ansible playbook for laravel installation
Simple playbook to install ngix,php,mysql,lavarel (from GitHub repo) and create *ubuntu* user for ssh access and sudo.
### How to run

- Ensure that ansible version is more than 2.9
- Ensure that ansible community.general collection installed
```console
ansible-galaxy install -r requirements.yml
```
- Create inventory file
- Fill hostvars (see example)
- Run ansible-playbook
```console
ansible-playbook -i inventory/<inventory name> main.yml
```
### ToDo

- Fix ansible-lint warnings (no-free-form and risky-file-permission)
- Think about idempotency in app role (maybe store APP_KEY in hostvars and proper git cloning)
- Add SSL
- Add payload app for db checking
