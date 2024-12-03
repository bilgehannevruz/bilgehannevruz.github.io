# iRODS Installation Guide

This guide provides instructions on how to install iRODS on your system.

## Prerequisites

- Supported operating system (e.g., CentOS, Ubuntu)
- Root or sudo access
- Network connectivity to download packages

## Download

You can see the latest information about packages here: [https://packages.irods.org/](https://packages.irods.org/)

### YUM package manager

1. Install public key and add repository

```bash
sudo rpm --import https://packages.irods.org/irods-signing-key.asc
wget -qO - https://packages.irods.org/renci-irods.yum.repo | sudo tee /etc/yum.repos.d/renci-irods.yum.repo
```

2. Install from the iRODS repository

```bash
sudo yum install irods-server irods-database-plugin-postgres rsyslog postgresql
```

## Installation

1. Setup `rsyslog`

- Create file `/etc/rsyslog.d/00-irods.conf`
```txt
$FileCreateMode 0644
$DirCreateMode 0755
$Umask 0000
$template irods_format,"%msg%\n"
:programname,startswith,"irodsServer" /var/log/irods/irods.log;irods_format & stop
:programname,startswith,"irodsDelayServer" /var/log/irods/irods.log;irods_format & stop
```

2. Restart rsyslog service.

```bash
sudo systemctl restart rsyslog
```

3. Setup `postgres`

- Become `postgres` user and run postgres.
```bash
sudo su - postgres && psql
```

```sql
CREATE USER irods WITH PASSWORD 'testpassword';
CREATE DATABASE "ICAT";
GRANT ALL PRIVILEGES ON DATABASE "ICAT" TO irods;
ALTER DATABASE "ICAT" OWNER TO irods;
```

- Confirm the permissions by running `\l`.
```bash
>>> \l
  Name    |  Owner   | Encoding | Locale Provider | Collate |  Ctype  | ICU Locale | ICU Rules |   Access privileges   
-----------+----------+----------+-----------------+---------+---------+------------+-----------+-----------------------
 ICAT      | irods    | UTF8     | libc            | C.UTF-8 | C.UTF-8 |            |           | =Tc/irods            +
           |          |          |                 |         |         |            |           | irods=CTc/irods
```


4. Initiate `setup_irods.py` 
```bash
sudo python3 /var/lib/irods/scripts/setup_irods.py < \
  /var/lib/irods/packaging/localhost_setup_postgres.input
```


## Start `iRODS` service
1. Starting the service
```bash
sudo su - irods -c "~/irodsctl -v start && ils"
```

2. Set the server name
```bash
sudo su - irods -c "iadmin set_delay_server $(hostname)"
```

3. Confirm that server is running
```bash
ps aux | grep irodsDelayServer
```
