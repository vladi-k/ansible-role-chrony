ansible-role-chrony
====

Install and configure chrony. 

Requirements
------------

* RHEL8

Role Variables
--------------

* `chrony_packages` - list of packages to install

Variables related to /etc/chrony.conf:

* `chrony_pools` - list of pools, example:

```yaml
chrony_pools:
  - name: 2.rhel.pool.ntp.org
    option: iburst
```

* `chrony_servers` - list of servers
* `chrony_driftfile` - driftfile
* `chrony_makestep` - makestep
* `chrony_rtcsync` - boolean to enable rtcsync
* `chrony_keyfile` - keyfile
* `chrony_leapsectz` - leapsectz
* `chrony_logdir` - logdir

Dependencies
------------

Collections:

* `ansible.builtin`


Example Playbook
----------------

```yaml
- hosts: my_servers
  roles:
    - ansible-role-chrony
```

License
-------

GPLv3

Author Information
------------------

Vladimir Vasilev (@vladi-k)
