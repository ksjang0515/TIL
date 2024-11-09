# Service won't start after install

## Background
- Installed `postgresql` by running `pacman -S postgresql`.
- `systemctl status postgresql` gave following result
```bash
× postgresql.service - PostgreSQL database server
     Loaded: loaded (/usr/lib/systemd/system/postgresql.service; disabled; preset: disabled)
     Active: failed (Result: exit-code) since Sun 2024-10-20 00:42:03 KST; 2min 36s ago
 Invocation: 0259d89aeb13443797a8e6ed986f321f
       Docs: man:postgres(1)
    Process: 10938 ExecStartPre=/usr/bin/postgresql-check-db-dir ${PGROOT}/data (code=exited, status=1/FAILURE)
   Mem peak: 1.8M
        CPU: 55ms

Oct 20 00:42:02 ArchServer systemd[1]: Starting PostgreSQL database server...
Oct 20 00:42:03 ArchServer postgres[10938]: "/var/lib/postgres/data" is missing or empty. Use a command like
Oct 20 00:42:03 ArchServer postgres[10938]:   su -l postgres -c "initdb --locale=C.UTF-8 --encoding=UTF8 -D '/var/lib/postgres/data'"
Oct 20 00:42:03 ArchServer postgres[10938]: with relevant options, to initialize the database cluster.
Oct 20 00:42:03 ArchServer systemd[1]: postgresql.service: Control process exited, code=exited, status=1/FAILURE
Oct 20 00:42:03 ArchServer systemd[1]: postgresql.service: Failed with result 'exit-code'.
Oct 20 00:42:03 ArchServer systemd[1]: Failed to start PostgreSQL database server.
```
- `systemctl start postgresql` gave following result
```
Job for postgresql.service failed because the control process exited with error code.
See "systemctl status postgresql.service" and "journalctl -xeu postgresql.service" for details.
```

## Troubleshooting
1. Switch to `postgres` user.
1. Run `initdb -D /var/lib/postgres/data`.
1. Return to regular user then start postgresql.
