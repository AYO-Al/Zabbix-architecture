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
```
3. 使用ansible为各个主机安装配置zabbix-agent2
```bash
ansible-playbook agent.yml -f 10
```

## 通用模板监控项
- 使用系统自带模板`Template os linux by zabbix agent`

## 负载均衡
- 监控项目
  - nginx，keepalived，端口，进程
  - nginx status(`Template App Nginx by Zabbix agent`)
  - tcp 连接状态11种
  - nginx访问日志中状态码
  - httpd整数状态是否过期
  - 其他待添加
  [Uploading image.png…]()
