Ansible Role: OpenStack Glance
==============================

This role installs and configures OpenStack Glance on EL7 system.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`)

    host: controller

Host that runs Glance services.

    mysql_host: controller
    mysql_password:

MySQL credentials.

    keystone_host: controller
    keystone_password:

Keystone credentials for Glance user.

    keystone_admin_password:

Password for admin Keystone user.

    region: RegionOne

OpenStack region.

    images:
      - name: CirrOS
        url:  http://download.cirros-cloud.net/0.3.4/cirros-0.3.4-x86_64-disk.img
        dest: /root/cirros-0.3.4-x86_64-disk.img

List of images to import into Glance.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - binarycode.openstack-glance

License
-------

BSD

Author Information
------------------

[Igor Sidorov](https://github.com/binarycode)
