# Install Oracle
1. Download Oracle RPM installation File (Oracle Installer)
2. Install RPM Installer with Root
3. Configure on progress
	* Configuration Instruction
	* start oracle xe
	* select configuration and next	
4. Select Application SQL*plus

## Install RPM Installer with Root
## Configure on progress
```java
 sudo dnf install ./oracle-xe-11.2.0-1.0.x86_64.rpm
```

#### configuration Instruction
```java
/etc/init.d/oracle-xe {start|stop|restart|force-reload|configure|status|enable|disable}
``` 

#### start oracle xe
```java
 /etc/init.d/oracle.xe start
```

#### select configuration and next.
```java
 /etc/init.d/oracle.xe configure
```

## Begin with Application SQL*plus
```java

SQL*Plus: Release 11.2.0.2.0 Production on Tue Mar 27 00:01:50 2018

Copyright (c) 1982, 2011, Oracle.  All rights reserved.

Use "connect username/password@XE" to connect to the database.
SQL> connect SYS as SYSDBA
Enter password: 
Connected to an idle instance.
SQL> conn hr/hr
ERROR:
ORA-01034: ORACLE not available
ORA-27101: shared memory realm does not exist
Linux-x86_64 Error: 2: No such file or directory
Process ID: 0
Session ID: 0 Serial number: 0


Warning: You are no longer connected to ORACLE.
SQL> connect SYS as SYSDBA
Enter password: 
Connected to an idle instance.
SQL> STARTUP
ORACLE instance started.

Total System Global Area 1068937216 bytes
Fixed Size		    2233344 bytes
Variable Size		  633342976 bytes
Database Buffers	  427819008 bytes
Redo Buffers		    5541888 bytes
Database mounted.
Database opened.
SQL> 
```
