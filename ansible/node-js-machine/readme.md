Ansible Basic Commands:
---------------

```
# ping all hosts
> ansible all -m ping 

# ping mailer host
> ansible mailer -m ping

# ping host as user
> ansible mailer -m ping -u root

# run playbook on all hosts as user
ansible-playbook playbooks/setup-user.yml -u root


```

Using my playbooks
-------------

```
# prepare host and create user juriy with keys
> ansible-playbook playbooks/setup-user.yml -u root

# update and setup new packages
> ansible-playbook playbooks/setup-dependencies.yml

# Setup node infrastructure (nvm, node.js 6 and 7, http-server, nodemon, pm2)
> ansible-playbook playbooks/setup-node.yml

# Setup MongoDB 
ansible-playbook playbooks/setup-mongo.yml

# Add another user
ansible-playbook playbooks/setup-other-user.yml

```