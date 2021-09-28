## Unit file for a services to run nginx server

> `Unit file` is a plain text ini-style that encodes information about a service, a socket, a device, a mount point, an automount point, a swap file or partition.

**Properties in unit file**

`[Unit]` carries generic information about unit that ts not dependent on type of unit.

`[Install]` section carries installation information for the unit. This section is not interpreted by systemd(1) during runtime, It is used by the enable & disable commands of systemctl(1) tool during installation of a unit.


### Example of service file to initiate a nginx server

**my-nginx-service.service**

```unit
[Unit]
Description=mynginx- server start

[Service]
type=forking
PIDFile=/run/nginx.pid
WorkingDirectory=/usr/sbin/
ExecStart=/usr/sbin/nginx
ExecReload=/usr/sbin/nginx -s reload
ExecStop=/bin/kill -s QUIT $MAINPID
PrivateTmp=true

[Install]
WantedBy=multi-user.target

```
Save this file in `etc/systemd/system`

To run this service
```
sudo systemctl start my-nginx-service.service
```
To see the status
```
sudo systemctl status my-nginx-service.service
```
**Output will look like**
```text
my-nginx-service.service - mynginx- server start
     Loaded: loaded (/etc/systemd/system/my-nginx-service.service; disabled; vendor preset: enabled)
     Active: active (running) since Tue 2021-09-28 12:17:21 IST; 7h ago
   Main PID: 1166 (nginx)
      Tasks: 0 (limit: 18772)
     Memory: 8.0K
     CGroup: /system.slice/my-nginx-service.service
             ‣ 1166 nginx: master process /usr/sbin/nginx -g daemon on; master_process on;

Sep 28 12:17:21 ubuntu nginx[31395]: nginx: [emerg] bind() to [::]:80 failed (98: Address already in use)
Sep 28 12:17:21 ubuntu nginx[31395]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Sep 28 12:17:21 ubuntu nginx[31395]: nginx: [emerg] bind() to [::]:80 failed (98: Address already in use)
Sep 28 12:17:22 ubuntu nginx[31395]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Sep 28 12:17:22 ubuntu nginx[31395]: nginx: [emerg] bind() to [::]:80 failed (98: Address already in use)
Sep 28 12:17:22 ubuntu nginx[31395]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Sep 28 12:17:22 ubuntu nginx[31395]: nginx: [emerg] bind() to [::]:80 failed (98: Address already in use)
Sep 28 12:17:23 ubuntu nginx[31395]: nginx: [emerg] bind() to 0.0.0.0:80 failed (98: Address already in use)
Sep 28 12:17:23 ubuntu nginx[31395]: nginx: [emerg] bind() to [::]:80 failed (98: Address already in use)
Sep 28 12:17:23 ubuntu nginx[31395]: nginx: [emerg] still could not bind()

```


## What does (5) mean in systemd.unit(5) ?

|  Number |  Meaning |
|----- | --------|
| 1 | General Commands |
| 2 | System Calls |
| 3 | Library functions, covering in particular the C standard library |
| 4 | Special files (usually devices, those found in /dev) and drivers |
| 5 | File formats and conventions |
| 6 | Games and screensavers |
| 7 | Miscellanea |
| 8 | System administration commands and daemons |
