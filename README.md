# rancher-install-master-ansible-role

Install rancher master, create global api key, configure default registry.


Requirements
------------
Docker must me installed on the host.

Role Variables
--------------

```
rancher_master_image: "rancher/server:{{ rancher_version }}"
rancher_agent_image: "rancher/agent:{{ rancher_agent_version }}"

rancher_version: "v1.6.10"
rancher_agent_version: "v1.2.6"

rancher_master_host: "localhost"
rancher_master_port: 8080
rancher_master_cluster_port: 9345
rancher_master_advertise_address: "{{ ansible_default_ipv4.address }}"
rancher_master_url: "http://{{ rancher_master_host }}:{{ rancher_master_port }}"

rancher_global_apikey_path: "{{ inventory_dir }}/group_vars/all/apikey"

rancher_default_username: "devops"
rancher_default_password: "changeme"

mysql_host: localhost
mysql_port: 3306
mysql_database: rancher
mysql_user: rancher
mysql_password: rancher

docker_registry: ""
```
License
-------

Apache License 2
