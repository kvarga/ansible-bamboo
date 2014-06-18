ansible-bamboo
==============

Bamboo Module for Ansible


How To Test:
```Shell
git clone git@github.com:ansible/ansible.git
ansible/hacking/test-module -m ./ansible-bamboo -a "passwd={pass} username={user} state={newstate} url={bamboo_url}"
```