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
  Port 2222
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile `pwd`/.vagrant/machines/dev/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL
EOS
```

## setup ssh-agent for sharing ssh-key for cloning GitHub private repos

* `ssh-agent`
* `ssh-add ~/.ssh/id_rsa`

## Using Vagrant

* Startup a development environment (default)

```
  vagrant up
  vagrant provision
```


(you need SSH keyset at ~/.ssh/id_rsa(.pub) and the key is registered on the gsplatform GitHub repo. )

After finished, please access to http://ckan:8000/

(you need to set ckan -> localhost setting on /etc/hosts)

* Startup a demo/production server(not yet implemented)

```
  vagrant up prod
  vagrant [ssh|halt|destroy] prod
```

## Add ckan admin

```
vagrant ssh dev
sudo su ckaner
cd /var/local/ckan/default/pyenv
. bin/activate
cd src/ckan
paster user add admin email=hal@georepublic.co.jp sysadmin=True
```

