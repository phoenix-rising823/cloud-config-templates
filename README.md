# cloud-config-templates

## Description

Cloud-init is normally used for the initial configuration for cloud instances (cloud virtual machines), however it can be used in the same means to provision VMs for on-premise hypervisors such as KVM, Proxmox, and XenServer. The cloud-config files are written in yaml and read from a "cloud drive" when a virtual machine is booted for the first time and provisioned in accordance to the cloud-config read by cloud-init.

This repo is a small collection of cloud-configs to for the initial configuration of VMs. Tested on the [xcp-ng](https://xcp-ng.org/) virtualization platform, but should work on other platforms as well. The OS this has been tested on is RHEL based (AlmaLinux to be exact), but the config for the base installation should work with just about any modern Linux distribution.

### Requirements

* A virtual machine template created with the [cloud-init](https://cloud-init.io/) package installed. *__NOTE__: The post [here](https://xen-orchestra.com/blog/centos-cloud-template-for-xenserver/) details setting up a fresh VM on xcp-ng and installing cloud-init and a couple other packages. I tested this on AlmaLinux and it worked as expected.*

### Notes

I haven't tested if these exact configurations will work with any cloud service provider yet, but they do work within the xcp-ng platform very well. For more information on usage, modules, or other configurations, see the [cloud-init documentation](https://cloudinit.readthedocs.io/en/latest/)