[![Support room on Matrix #nextcloud-docker-ansible:matrix.org](https://img.shields.io/matrix/nextcloud-docker-ansible:matrix.org.svg?label=%23nextcloud-docker-ansible:matrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#nextcloud-docker-ansible:matrix.org)


-------
This is a fork of the [abandoned Playbook](https://github.com/spantaleev/nextcloud-docker-ansible-deploy)  
This fork aims using an external Nginx Proxy. All other paths like internal nginx-proxy should work, but aren't maintained well. You are free to help changing this and more ;)  
If you are a beginner and just want use Nextcloud or want to use Traefik, I recommend the official successor [MASH playbook](https://github.com/mother-of-all-self-hosting/mash-playbook)!

-------

# Nextcloud (A safe home for all your data) server setup using Ansible and Docker

This [Ansible](https://www.ansible.com/) playbook can help you set your own [Nextcloud](https://nextcloud.com/) server:

- on your own Debian/CentOS/RedHat server

- with all services ([Nextcloud](https://nextcloud.com/), [PostgreSQL](https://www.postgresql.org/), [Traefik](https://traefik.io), [OnlyOffice](https://www.onlyoffice.com/), etc.) running in [Docker](https://www.docker.com/) containers

- powered by [the official Nextcloud container image](https://hub.docker.com/_/nextcloud)

- [interoperates nicely](docs/configuring-playbook-interoperability.md) with [related](#related) Ansible playbooks or other services using Traefik for reverse-proxying

SSL certificates are automatically managed by a [Traefik](https://traefik.io) reverse-proxy.

Various components (Postgres, Traefik, etc.) can be disabled and replaced with your own other implementations (see [configuring the playbook](docs/configuring-playbook.md)).


## Features

Using this playbook, you can get the following services configured on your server:

- a [Nextcloud](https://nextcloud.com/) server - storing your data

- (optional) a [PostgreSQL](https://www.postgresql.org/) database for Nextcloud

- (optional) free [Let's Encrypt](https://letsencrypt.org/) SSL certificate, which secures the connection to the Nextcloud server

- (optional) [OnlyOffice](https://www.onlyoffice.com/) integration - for online document editing/previewing

- (optional) [Collabora Online](https://www.collaboraoffice.com/) integration - for online document editing/previewing

Basically, this playbook aims to get you up-and-running with all the basic necessities around Nextcloud.


## Installing

To configure and install Nextcloud on your own server, follow the [README in the docs/ directory](docs/README.md).


## Changes

This playbook evolves over time, sometimes with backward-incompatible changes.

When updating the playbook, refer to [the changelog](CHANGELOG.md) to catch up with what's new.


## Support

- Matrix room: [#nextcloud-docker-ansible:matrix.org](https://matrix.to/#/#nextcloud-docker-ansible:matrix.org)

- Github issues: [JokerGermany/nextcloud-docker-ansible-deploy/issues](https://github.com/JokerGermany/nextcloud-docker-ansible-deploy/issues)


## Related

You may also be interested in these other playbooks:

- [matrix-docker-ansible-deploy](https://github.com/spantaleev/matrix-docker-ansible-deploy) - for deploying a fully-featured [Matrix](https://matrix.org) homeserver
