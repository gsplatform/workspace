# Development Worksapce

This repository is devoted to the development and deployment of CKAN
The reason for its existance is:

* to manage issues regarding the deployment
* to provide setup scripts (e.g based on ansible) for this deployment
* to setup a development environment using Vagrant

## Getting Started

* Install Vagrant
* Install Ansible `pip install ansible`

* `git clone git@github.com:gsplatform/workspace.git`
* `cd workspace`

## setup configuration for ansible

```
cat << EOS >> ~/.ssh/config
Host dev
  HostName 127.0.0.1
  User vagrant
  Port 2200
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile `pwd`/.vagrant/machines/dev/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL
EOS
```

## Using Vagrant

* Startup a development environment (default)

  vagrant up
  vagrant [ssh|halt|destroy]

(you need SSH keyset at ~/.ssh/id_rsa(.pub) and the key is registered on the gsplatform GitHub repo. )

* Startup a demo/production server

  vagrant up prod (not yett implemented)
  vagrant [ssh|halt|destroy] prod

