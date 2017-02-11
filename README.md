# ansible-server-init
Initializes a newly provisioned ubuntu server with a non-root user and latest system 
updates

Variables required are:

`user` - The non-root user to be created

`password` - The crypted password for the user
(see: https://docs.ansible.com/ansible/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module)

In addition, a file `authorized_keys` needs to be provided under the `files` directory
containing ssh public keys for persons authorized to log in as the created user

An example playbook `init-server.example.yml` that uses this role is provided.
