Ansible Role: Active Directory
=========

Ansible role to configure Active Directory Authentication on Linux servers.

Requirements
------------

The role does not require anything to run on RHEL and its derivatives.

Role Variables
--------------

Available variables are listed below, along with default values (see ```defaults/main.yml```):

``` yaml
service_domain: "example.com"
service_account: "myuser"
service_password: "mypassword"
ou: "OU=Computers, DC=example, DC=com"
```

```service_domain``` **(Required)** The name of the active directory domain

```service_account``` **(Required)** The service user account to use when joining the host to the active directory domain

```service_password``` **(Required)** The password of the specified service user account

```ou``` **(Required)** The Organizational Unit where to create the hosts machine account in the active directory domain

Role variables can be stored with the hosts.yaml file, or in the main variables file.

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
    - hosts: servers
      roles:
         - role: mikepruett3.active-directory
```

License
-------

MIT

Author Information
------------------

Role created by [mikepruett3](https://github.com/mikepruett3) on [Github.com](https://github.com/mikepruett3/ansible-role-active-directory)
