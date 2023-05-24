# Zabbix-architecture
使用zabbix监控架构，监控各主机服务

## 服务配置
1. 安装配置zabbix-server
2. 修改/conf/zabbix_agent2.conf
```bash
Server=Server_ip
ServerActive=Server_ip
HostnameItem=system.hostname
HostMetadataItem=system.hostname
3. 使用ansible为各个主机安装配置zabbix-agent2
```bash
ansible-playbook agent.yml -f 10


## 监控

