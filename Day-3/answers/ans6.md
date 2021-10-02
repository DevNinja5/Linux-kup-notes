# Que 6: How can we persist rules in iptables?

Persisting rules in iptables mean to store the rules in `/etc/iptables/rules.v4` for ipv4 and `/etc/iptables/rules.v6` for ipv6 .The iptables-persistent package should be pre installed. It prevents rules to get wipe-out when system reboots.

**Commands to Persist ip rules
```
 sudo netfilter-persistent save
```
OR
```
sudo iptables-save > /etc/iptables/rules.v4
```
