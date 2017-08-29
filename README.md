# ansible-fedcloud-h2oai

Ansible playbook for configuring h2oai on fedcloud

## Variables

The `group_vars/all.yml` file contains the variables that need to be configured for the playbook to work. The `h2oai_password` will be the password used to login to jupyter and to the h2oai server. Do not use a valuable password since the h2oai server is on bare HTTP.

## Inventory

The playbook expects an inventory similar to this:
```
[all]
host1
host2
host3


[master]
host1
```

The master is where jupyter will be installed and the one with the public IP. The others do not need to be publicly accessible 

## Applying the playbook

Just run ansible as usual:
```
ansible-playbook -i inventory play.yml
```


## TODO
Convert this into a proper role
