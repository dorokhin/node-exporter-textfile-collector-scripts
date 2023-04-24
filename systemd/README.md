# Systemd example

```console
sudo nano /etc/systemd/system/smartctl_textfile_collector.timer
```

```console                                                
[Unit]
Description=Run smartctl_textfile_collector

[Timer]
OnCalendar=*-*-* *:*:00

[Install]
WantedBy=timers.target
```

Edit (create) service file:
```console          
sudo nano /etc/systemd/system/smartctl_textfile_collector.service
```


Enable timer:
```console
sudo systemctl daemon-reload
sudo systemctl enable --now  smartctl_textfile_collector.timer
systemctl list-timers --all
```
