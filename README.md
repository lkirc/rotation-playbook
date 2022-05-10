# rotation-playbook
This is an Ansible playbook designed to allow you to change the passwords and SSH keys of an entire fleet of machines. Given what it does, it should be used with care, but I use it personally in my own lab and am reasonably confident it's reliable. ** Use with care. ** 

## Usage
It's highly recommended you create SSH keys and setup key-based SSH access to all hosts you want to manage, rather than relying on passwords. This is a good idea in general, but especially a good idea when you plan to change a bunch of passwords.

Nevertheless, you should be able to use this playbook as follows:
* ansible-playbook site.yml --ask-pass --ask-become-pass

The playbook will ask you for the new password you want to set, then set it on all the hosts you're connecting to for the user you're connecting as. That's it.