

## Lightweight Monitoring of Adaptec RAID Controller Using arcconf
- Controllers
- Volumes
- Disks

----

### Copy arcconf
```bash
cp ./additionally/cmdline/arcconf /usr/sbin/arcconf
chmod +x /usr/sbin/arcconf
```

### Copy UserParameters

```bash
cp ./zabbix_agent.conf.d/adaptec.conf /etc/zabbix/zabbix_agent.conf.d/adaptec.conf
```

or

```bash
cp ./zabbix_agent.conf.d/adaptec.conf /etc/zabbix/zabbix_agent.d/adaptec.conf
```

### Copy Sudoers File

```bash
cp ./sudoers.d/zabbix_adaptec  /etc/sudoers.d/zabbix_adaptec
```

### Restart Zabbix Agent

```bash
systemctl restart zabbix-agent
```
----

### Zabbix Server Web Interface

- Import the template into Zabbix.
- Attach the template to the host.


Example JavaScript can be found in `additionally/js in template`.

### See more information in the 'Latest Data' menu in the web interface of the Zabbix Server.