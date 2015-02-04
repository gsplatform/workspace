# Development Worksapce

This repository is devoted to the development and deployment of PublicaMundi.
The reason for its existance is:

* to manage issues regarding the deployment
* to provide setup scripts (e.g based on ansible) for this deployment  
* to setup a development environment using Vagrant

## Getting Started

* Install Vagrant
* Install Ansible `pip install ansible`

## Using Vagrant

* Startup a development environment (default)

	vagrant up
	vagrant [ssh|halt|destroy]

* Startup a demo/production server 

	vagrant up prod
	vagrant [ssh|halt|destroy] prod
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
