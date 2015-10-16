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
  vagrant [ssh|halt|destroy]
```

(you need SSH keyset at ~/.ssh/id_rsa(.pub) and the key is registered on the gsplatform GitHub repo. )

* Startup a demo/production server

```
  vagrant up prod (not yett implemented)
  vagrant [ssh|halt|destroy] prod
```

For some reason the ansible script hangs at installing ckanext-datastorer requrement modules.
So I commented out the process.
You have to install it manually after provisioning.

```
  vagrant ssh dev
  %(remote host) sudo su - ckaner
  %(remote host) cd /var/local/ckan/default/pyenv/
  %(remote host) . bin/activate
  %(remote host) cd src/ckanext-datastorer
  %(remote host) pip install -r pip-requirements.txt
```


#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
#------------------------------------------------------------------------------
# Customize for your needs
# Commented out to run on VirtualBox, platform Linux
#------------------------------------------------------------------------------

#default_statistics_target = 100
#maintenance_work_mem = 352MB
#checkpoint_completion_target = 0.9
#effective_cache_size = 4GB
#work_mem = 28MB
#wal_buffers = 16MB
#checkpoint_segments = 32
#shared_buffers = 1408MB
