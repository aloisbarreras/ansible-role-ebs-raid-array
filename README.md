ansible-role-ebs-raid-array
---------------------------
Ansible role to create an EBS backed RAID array on an EC2 instance.

Requirements
------------

None.

Role Variables
--------------

    raid_dev: /dev/md0
    raid_level: 0
    raid_name: RAID
    raid_mount: /mnt/md0
    raid_devices:
      - /dev/xvdf
      - /dev/xvdg

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: aloisbarreras.ebs-raid-array
           raid_dev: /dev/md0
           raid_level: 0
           raid_mount: /mnt/my-mount

License
-------

MIT

Author Information
------------------

Alois <aloisbarreras@icloud.com>

Credit
------
Created with help from the [official AWS docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/raid-config.html) and this [gist](https://gist.github.com/akabe/7d85b610c6005d08d655b0666ae8afe2).
