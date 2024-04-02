ansible-role-satellite
=========

A role for deploying Red Hat Satellite.

Requirements
------------

* python >= 2.7


Role Variables
--------------

    rhn_username: user
    rhn_password: password

    sat_username: admin
    sat_password: redhat

    sat_org: NASA_JPL
    sat_location: Pasadena

    sat_version: 6.14

Optional Vars

    # Use this variable to change the pool_id used for the Red Hat Satellite subscription 
    pool_id: 2c946de78e8076d6018e8469c0ee0dc5

    # Use this if you do not have DNS records in place to configure /etc/hosts
    sat_hostname: satellite.example.com

Example Playbook
----------------

    - hosts: all
      roles:
        - ansible-role-satellite

License
-------

MIT/BSD

Author Information
------------------

This role was created by [Michael Tipton](https://ibeta.org).
