### Install zabbix agent on RHEL 7 hosts

#### Before you begin

Validate that server has access to zabbix repo:

```ini
$ curl -k https://repo.zabbix.com
$ nc -zvw 1 repo.zabbix.com 443
```

Validate that same environment servers have same sudo user and password

<br>

Configure [hosts.ini](hosts.ini) file

Edit variables for your needs in files:

```ini
./roles/zabbix/vars/main.yml
```

<br>

#### Run installation playbook

```shell
$ ansible-playbook zabbix.yml
```