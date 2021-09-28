## Que :How to check which ports are being used by which process?
### Using lsof command

```
lsof -i -P -n | grep -i "listen"
```

where,
- `-i` : Look for listing ports
- `-P` : Inhibits the conversion of port numbers to port names for network files.
- `-n` : Do not use DNS name

### Using netstat command

```
sudo netstat -tulpn | grep LISTEN
```
where,
- `-t` : All TCP ports
- `-u` : All UDP ports
- `-l` : display listening server
- `-p` : show PID & name
- `-n` : Don't resolves names & show ip `localhost` -> `127.0.0.1`
