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

## Usage
* Install the role (either from Galaxy or directly from GitHub)
* Copy the defaults file to your inventory (or wherever you store them) and
  fill in the blanks
* Add the role to your master playbook
* Run Ansible
* ???
* Profit!
