Ansible Role: Common
====================

Role to deploy common tools and users setup on CentOS

Requirements
------------

Ansible 2.4 must be installed in the host where the playbook will be executed.
This role will then need to be installed via ansible-galaxy as port of roles requirement.


Role Variables
--------------

- **absent_users**: Users to be removed from the host i.e "Centos"
- **package_absent_list**: List of packages to be removed.
- **package_absent_exclusion_list**: List of packages to be excluded from removal.
- **package_common_list**: List of packaged to be installed as part of base operational packages
- **present_users**: List of users to be created on the host
- **sudoers_groups**: List of user groups to be added onto sudoers list
- **timezone**: Default to "Europe/London"

Dependencies
------------

None


Example GitLab Token Access Usage
---------------------------------

```
git clone git clone https://oauth2:<personal_access_token>@github.com/dusnguyen/ansible-common.git
```

Example Playbook
----------------

main.yml playbook
```
    - name: Install Gitlab
      hosts: gitlab
      roles:
        - common
        - gitlab
      tags:
        - gitlab
```

To Do
-----

License
-------

BSD
MIT

Author Information
------------------

Dustin Nguyen - dustin.nguyen
