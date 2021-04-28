# satellite_register - registers a host with Red Hat Satellite 6

## Synopsis
An Ansible role for registering hosts with Red Hat Satellite 6 using Activation Key(s).

## Options

| Parameter                         | Required | Default | Example    | Comments                                            |
|-----------------------------------|----------|---------|------------|-----------------------------------------------------|
| satellite\_fqdn                   | yes      |         | sat6-master-01.example.com | FQDN of Satellite server. Used for URL buildout     |
| satellite\_org                    | yes      |         | ACME | Satellite Organization to join.                     |
| satellite\_location               | yes      |         | DEV | Satellite Location to join.                         |
| satellite\_hostgroup              | yes      | false   | false | Satellite Location to join.                         |
| satellite\_registration\_user     | yes*     |         | satellite.service | Only required if you specify a hostgroup and are not doing the manual registration tasks. User to view API with. Recommend a service account. |
| satellite\_registration\_password | yes*     |         | <omitted> | Only required if you specify a hostgroup and are not doing the manual registration tasks. Admin Password to use. Store this in VAULT.         |
| satellite\_activation\_key        | yes      |         | AK_RHEL_7_SRV_BASE_DEV | Satellite Activation Keys to register with.         |
| satellite\_auto\_subscribe        | no       | no | no | Whether or not to auto subscribe on registration    |
| satellite\_update\_packages       | no       | no | no | Whether or not to update all pacakges on host       |


This role includes a python script generated by Satellite. For more details and requirements,
please references: https://access.redhat.com/articles/2280691
