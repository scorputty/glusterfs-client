GlusterFS Client
=========

Setup GlusterFS client using Ansible Tower.

Requirements
------------

A running GlusterFS environment to connect with...

## Role Variables

    defaults/main.yml
    gluster_package_version: '37'
    gluster_volume_name: "tri-repvol01"
    gluster_server_name: "ansiblehost22"
    gluster_share_dir: "/glusterfs/share"
    gluster_share_user: "vagrant"
    gluster_share_group: "root"
    gluster_share_perm: "750"


Dependencies
------------

none

## Example Playbook site.yml

    - hosts: glusterfs_client_group
      strategy: free
      gather_facts: true
      roles:
        - role: glusterfs-client

License
-------

GPLv2

Author Information
------------------

More info about GlusterFS here:
https://gluster.readthedocs.io/en/latest/
