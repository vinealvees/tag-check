Role Name
=========

This role can add/remove/list tags on EC2 instances and volumes

Requirements
------------

Role tested in Ansible 2.9.6, Python 3.8.5.
For more details, check modules [ec2_instance_info](https://docs.ansible.com/ansible/2.9/modules/ec2_instance_info_module.html), [ec2_tag](https://docs.ansible.com/ansible/2.9/modules/ec2_tag_module.html), [ec2_vol_info](https://docs.ansible.com/ansible/2.9/modules/ec2_vol_info_module.html)

Role Variables
--------------

defaults/main.yml
```
AWSAccessKey: aws_access_key_id
AWSSecretAccessKey: aws_secret_access_key
AWSRegion: aws_region
```

Example Playbook
----------------

```
- name: Setting Tags on EC2 instances and volumes
  hosts: localhost
  connection: local
  environment:
    AWS_ACCESS_KEY_ID: '{{ AWSAccessKey }}'
    AWS_SECRET_ACCESS_KEY: '{{ AWSSecretAccessKey }}'
    AWS_DEFAULT_REGION: '{{ AWSRegion }}'
  roles:
    - tag-check
```

License
-------

BSD

Author Information
------------------

Github: [vinealvees](https://github.com/vinealvees)
