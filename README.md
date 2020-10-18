# ansible-zabbix-web-nginx-mysql
Deploy docker container with web server for zabbix (nginx) based on official zabbix-web-nginx-mysql container (https://hub.docker.com/r/zabbix/zabbix-web-nginx-mysql).

## Role variables
| Variable | Default value | Description |
| :---:        |     :---:      |         :---: |  
service_name                    |       zabbix-web-docker               |   Service name in OS
uninstall_service               |       false                           |
DB_SERVER_HOST                  |       mysql-docker                    |   MySQL-server host hostname
ZBX_SRV                         |       zabbix-srv-docker               |   Zabbix-server host hostname
DB_CONTAINER                    |       mysql                           |   MySQL-server docker container name 
ZBX_SRV_CONTAINER               |       zabbix-server                   |   Zabbix-server docker container name 
web_host_port                   |       80                              |   Host network port
web_container_port              |       8080                            |   Container network port
port_type                       |       tcp                             |   Port type
docker_image                    |       zabbix/zabbix-web-nginx-mysql   |   Docker image (https://hub.docker.com/)

### How to use
    - installation: just start the role
    - uninstallation: add --extra-vars "uninstall_service=true"