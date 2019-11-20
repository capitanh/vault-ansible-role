Role Name
=========
This role will download and install Hashicorp Vault and Hashicorp Consul as backend storage system

Requirements
------------
None

Role Variables
--------------
This role requires the following variables to be defined elsewhere in the playbook that uses it:
```yaml
  vault_version:    1.3.0         # Vault version
  vault_port:       8200          # Default http interface port
  install_dir:      /usr/bin      # Default directory for executables

  consul_data_dir:  /opt/consul   # Data directory for consul
  consul_user:      consul        # Sustem user to run consul service
  consul_version:   1.6.2         # Consul version
  consul_port:      8500          # Consul listener port
```
All of them have the specified default values already set. You only need to declare another value if it's going to be overriden.

Dependencies
------------
None

Example Playbook
----------------
Register the role in requirements.yml:
```yaml
    - src: capitanh.vault-ansible-role
      name: vault
```
Include it in your playbooks:
```yaml
    - hosts: servers
      roles:
      - vault
```
License
-------
BSD
