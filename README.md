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
