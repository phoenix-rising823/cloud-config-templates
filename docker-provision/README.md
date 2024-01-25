# docker-provision

## Description

This cloud-config is meant to install and configure docker on an instance running AlmaLinux/Rocky Linux.

For hosts running Fedora Linux make use the Fedora repo make this change:

```console
sudo dnf config-manager --add-repo https://download.docker.com/linux/fedora/docker-ce.repo
```
The firewall configuration adds ports for the use of Docker in Swarm mode, if you're not using Swarm, then remove the firewall commands can be removed (I removed cockpit from the services, as there's no real need for it here).

Follow the Docker [documentation](https://docs.docker.com/reference/) for more information.


### Requirements

* See the the README.md found at the root of the [cloud-config-template repo](https://github.com/phoenix-rising823/cloud-config-templates/blob/main/REAMDME.md)