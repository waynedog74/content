---
Title: "PostgreSQL basic commands"
Date: 2017-06-01 20:06:32
Categories: [data base]
tags: [postgresql]
Authors: sedlav
---

## Connect to the database with default user

```sh
$ sudo -u postgres psql
```

## Create user

```sql
CREATE USER username WITH PASSWORD 'MYPASS';
```

You must edit pg_hba.conf in Debian/Ubuntu you have this dir structure:

```
/etc/postgresql/
└── 9.5
    └── main
        ├── environment
        ├── pg_ctl.conf
        ├── pg_hba.conf
        ├── pg_ident.conf
        ├── postgresql.conf
        └── start.conf
```

The above file looks like this:

```
# PostgreSQL Client Authentication Configuration File
#
# ...
#
# local      DATABASE  USER  METHOD  [OPTIONS]
# host       DATABASE  USER  ADDRESS  METHOD  [OPTIONS]
# hostssl    DATABASE  USER  ADDRESS  METHOD  [OPTIONS]
# hostnossl  DATABASE  USER  ADDRESS  METHOD  [OPTIONS]
#
# ...
# 
# METHOD can be "trust", "reject", "md5", "password", "gss", "sspi",
# "ident", "peer", "pam", "ldap", "radius" or "cert".  Note that
# "password" sends passwords in clear text; "md5" is preferred since
# it sends encrypted passwords.
#
# ...
#
# Database administrative login by Unix domain socket
local   all             postgres                                peer

# TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all             all                                     peer
# IPv4 local connections:
host    all             all             127.0.0.1/32            md5
host    breinty_db      breinty         127.0.0.1/32            md5
# IPv6 local connections:
host    all             all             ::1/128                 md5
# Allow replication connections from localhost, by a user with the
# replication privilege.
#local   replication     postgres                                peer
#host    replication     postgres        127.0.0.1/32            md5
#host    replication     postgres        ::1/128                 md5

```

Then add your own rule to it.

## Set super privileges to specific user

```sql
ALTER USER username WITH SUPERUSER;
```

## Create a database

```sql
CREATE DATABASE dbname OWNER username;
```

## Drop database

```
DROP DATABASE dbname;
```

## List databases

```
\l
```

## Import a data base

```
$ psql username  -h hostname -d dbname < dump.sql
```

## Change DATABASE

```
\c dbname;
```

## Create Postgis extension

```sql
CREATE EXTENSION Postgis;
```

## List tables

```
\dt
```

## Quit from Postgre console

```
\q
```
