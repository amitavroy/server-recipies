# Server clean up commands

A set of clean up commands which can be executed on server to remove unwanted space and general maintenance

## systemd 
It collects logs from all processes, applications of the system every second which starts from the boot. 
All these logging events are managed by journald daemon of systemd. The journald collects all the logs (info, warnings, errors, etc) and stores them 
as binary data in the disk files. 

### Check the disk usage of systemd on your system

```
journalctl --disk-usage
```

### We can also configure systemd by tweaking this well documented config file
```
/etc/systemd/journald.conf
SystemMaxUse=500M
```

### And, if you want to manually delete logs till certain days
```
journalctl --vacuum-time=28d
```
