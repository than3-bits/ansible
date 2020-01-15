# ansible
repository of personal ansible playbooks

bootstrap.yml

Description: Ensure ansible node has all pre-requisites needed for runtime.

* Install Python 2.7 Dependency
* Install Python PIP and SimpleJSON Modules
* Set Non-interactive for Ipv4/Ipv6 persistent tables
* Install iptables-persistent package.
* Install iptables_raw ansible module (Requires Iptables-persistent).

bootstrap-aaa.yml

Description: Set up account authentication

* Creates Remote Administration Group 
* Creates Service Account.
* Adds Remote Administration Group to sudoers
* Adds Service Account to Remote Administration Group
* Adds Service Account certificate to SSH for future passwordless login

docker.yml

Description: Install Docker Community Edition and repository

* Install Docker Dependencies (
apt-transport-https ca-certificates curl gnupg-agent software-properties-common )
* Install Docker GPG key to APT
* Add Docker Repository
* Install Docker Community Edition
* Run Docker Hello-World
* Register Stat of Hello-World

docker-sto-migrate.yml

Description: Migrate Docker Storage Path to new path

* Stop Running Docker Services
* Tar Default Path (for backup)
* Check New Path, if not exist create
* Copy Docker to New Path
* Setup Docker Symlink from New path to /var/lib/docker


Re: iptables_raw.py
There is some confusion over what license should apply to the ansible iptables_raw.py module. The original source is available from Nordeus. Their github account is located at:

https://github.com/Nordeus/ansible_iptables_raw

I've opened an issue up regarding the missing license with them [here](https://github.com/Nordeus/ansible_iptables_raw/issues/29) and am awaiting a response.
