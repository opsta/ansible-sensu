# Ansible Role: sensu

ansible roles for install Sensu

Your inventory should be like this for select roles for Sensu
  - sensu-server is a group of sensu-server and sensu-api
  - sensu-client is a group of sensu-client

Example of inventory
```ini
sensu-0 ansible_host=xx.xx.xx.xx ansible_user=user
sensu-1 ansible_host=yy.yy.yy.yy ansible_user=user

[sensu-server]
sensu-0

[sensu-client]
sensu-0
sensu-1

[sensu:children]
sensu-server
sensu-client
```

## Requirements

None.

## Role Variables



## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - opsta.sensu


## License

MIT

## Author Information

Opsta (Thailand) Co.,Ltd.
