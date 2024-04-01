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

    # Use this list variable to override the default ports opened for firewalld
    firewalld_ports:
      - http
      - https
      - dns
      - dhcp
      - 5647/tcp
      - 8000/tcp
      - 8140/tcp
      - 9090/tcp
      - 5000/tcp

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
