## Example Output
```
abendale@itool.id@a024:~/scripts$ rmess messages.log 

Report for log file: /var/log/messages.log
-----------------------------------
Total lines: 32
HostName : server-prod-01
Start Date: May 23 22:51:33
End Date: May 23 23:15:00
Top 10 Processes:
-----------------------------------
     10 systemd[1]:
      3 sudo[31201]:
      3 kernel:
      2 sshd[31002]:
      2 sshd[30455]:
      2 nginx[884]:
      2 chronyd[812]:
      1 systemd-resolved[652]:
      1 sshd[30412]:
      1 python3[4102]:
-----------------------------------
Error Counts: 7
Warning Counts: 3
Info Counts: 1
-----------------------------------
Top 10 Processes(Errors):
-----------------------------------
      1 systemd-resolved[652]:
      1 sshd[30455]:
      1 python3[4102]:
      1 nginx[884]:
      1 mysqld[1022]:
      1 kernel:
      1 backup-script[30501]:
-----------------------------------
Top 10 Processes(Warnings):
-----------------------------------
      1 sshd[30412]:
      1 mysqld[1022]:
      1 kernel:
-----------------------------------
Top 10 Processes(Info):
-----------------------------------
      1 NetworkManager[712]:
-----------------------------------
```

## Example output with -e (show errors)
```
abendale@itool.id@a024:~/scripts$ rmess -e messages.log 

Report for log file: /var/log/messages.log
-----------------------------------
Total lines: 32
HostName : server-prod-01
Start Date: May 23 22:51:33
End Date: May 23 23:15:00
Top 10 Processes:
-----------------------------------
     10 systemd[1]:
      3 sudo[31201]:
      3 kernel:
      2 sshd[31002]:
      2 sshd[30455]:
      2 nginx[884]:
      2 chronyd[812]:
      1 systemd-resolved[652]:
      1 sshd[30412]:
      1 python3[4102]:
-----------------------------------
Error Counts: 7
Warning Counts: 3
Info Counts: 1
-----------------------------------
Top 10 Processes(Errors):
-----------------------------------
      1 systemd-resolved[652]:
      1 sshd[30455]:
      1 python3[4102]:
      1 nginx[884]:
      1 mysqld[1022]:
      1 kernel:
      1 backup-script[30501]:
-----------------------------------
Top 10 Processes(Warnings):
-----------------------------------
      1 sshd[30412]:
      1 mysqld[1022]:
      1 kernel:
-----------------------------------
Top 10 Processes(Info):
-----------------------------------
      1 NetworkManager[712]:
-----------------------------------
-----------------------------------
Error messages for process: systemd-resolved[652]:
-----------------------------------
May 23 22:54:10 server-prod-01 systemd-resolved[652]: Server returned error NXDOMAIN, mitigating potential DNS violation DVE-2018-0001, retrying transaction with reduced feature level UDP.
-----------------------------------
-----------------------------------
Error messages for process: sshd[30455]:
-----------------------------------
May 23 22:51:33 server-prod-01 sshd[30455]: error: maximum authentication attempts exceeded for root from 192.168.1.155 port 45123 ssh2
-----------------------------------
-----------------------------------
Error messages for process: python3[4102]:
-----------------------------------
May 23 22:55:40 server-prod-01 python3[4102]: ERROR: root: Could not establish connection to Redis cache cluster. Timeout exceeded.
-----------------------------------
-----------------------------------
Error messages for process: nginx[884]:
-----------------------------------
May 23 22:53:22 server-prod-01 nginx[884]: [error] 884#884: *14502 connect() failed (111: Connection refused) while connecting to upstream, client: 203.0.113.50, server: app.example.com, request: "GET /api/v1/users HTTP/1.1", upstream: "http://127.0.0.1:8080/api/v1/users"
-----------------------------------
-----------------------------------
Error messages for process: mysqld[1022]:
-----------------------------------
May 23 22:51:10 server-prod-01 mysqld[1022]: 2026-05-23T22:51:10.123456Z 0 [Warning] Aborted connection 1542 to db: 'app_db' user: 'db_user' host: '10.0.1.5' (Got an error reading communication packets)
-----------------------------------
-----------------------------------
Error messages for process: kernel:
-----------------------------------
May 23 22:50:45 server-prod-01 kernel: [ 4512.103422] EXT4-fs (sdb1): warning: mounting fs with errors, running e2fsck is recommended
-----------------------------------
-----------------------------------
Error messages for process: backup-script[30501]:
-----------------------------------
May 23 22:52:14 server-prod-01 backup-script[30501]: ERROR: Backup failed. Destination path /mnt/backup/storage is read-only.
-----------------------------------
```
