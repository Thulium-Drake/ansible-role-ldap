[![Build Status](https://drone.element-networks.nl/api/badges/Element-Networks/ansible-role_ldap/status.svg)](https://drone.element-networks.nl/Element-Networks/ansible-role_ldap)

# LDAP role
This role will join a Debian or RedHat machine to bind against a LDAP directory.

## Configuration steps
This role will configure the following programs to prepare your system for LDAP
authentication:

* Oddjob (only for RHEL)
* OpenLDAP (only plain LDAP or STARTTLS is supported)
* PAM
* SSSD
* AutoFS (if enabled)

It will also configure sudo permissions for a user-specified LDAP group. The
default permissions given to this group is:

```
ALL=(ALL) ALL:NOPASSWD
```

## Server
This role can also be used to install an LDAP server on Debian 10. Ubuntu 18.04,
20.04 and CentOS 7, 8 are not supported.

The server installation comes with decent SSL and LDAP hardening settings.

The client part of this role is compatible and can be used right away.

## Usage
* Install the role (either from Galaxy or directly from GitHub)
* Copy the defaults file to your inventory (or wherever you store them) and
  fill in the blanks
* Add the role to your master playbook
* Run Ansible
* ???
* Profit!
