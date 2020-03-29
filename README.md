pcopfer.openssh
===============

A role to install and manage openssh.

Role Variables
--------------

- ``openssh_ssh_users: ...``  Users with ssh_keys witch are allowd to login via ssh, see Example
- ``openssh_sshd_port: 22`` Port for ssh
- ``ufw_ssh_public: true`` Open TCP sshd_port in Firewall

Example Playbook
----------------

    - hosts: servers
      vars:
         - openssh_ssh_users:
	   - name: "test"
	     key: "{{ pubkey_test_vault }}"
	   - name: "foo"
	     key: ""ssh-rsa AAAA..."
      roles:
         - role: pcopfer.openssh

License
-------

BSD

Author Information
------------------

pcopfer <christian-platz at pcopfer.de>
With help from rixx <r at rixx.de>
