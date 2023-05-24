# Zabbix-architecture
使用zabbix监控架构，监控各主机服务
1. 安装配置zabbix-server
2. 使用ansible为各个主机安装配置zabbix-agent2
```bash
ansible-playbook agent.yml -f 10

