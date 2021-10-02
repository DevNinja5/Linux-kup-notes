# Que 2: What is prot, opt, in, out, source & destination? 

**Command** 
```
sudo iptables -L -v
```

**Output**
```text
Chain INPUT (policy ACCEPT 334K packets, 400M bytes)
 pkts bytes target     prot opt in     out     source               destination         
  335 20100 DROP       all  --  any    any     edge-star-mini-shv-01-del1.facebook.com  anywhere            

Chain FORWARD (policy ACCEPT 0 packets, 0 bytes)
 pkts bytes target     prot opt in     out     source               destination         
    0     0 DOCKER-USER  all  --  any    any     anywhere             anywhere            
    0     0 DOCKER-ISOLATION-STAGE-1  all  --  any    any     anywhere             anywhere            
    0     0 ACCEPT     all  --  any    docker0  anywhere             anywhere             ctstate RELATED,ESTABLISHED
    0     0 DOCKER     all  --  any    docker0  anywhere             anywhere            
    0     0 ACCEPT     all  --  docker0 !docker0  anywhere             anywhere            
    0     0 ACCEPT     all  --  docker0 docker0  anywhere             anywhere            
    0     0 ACCEPT     all  --  any    docker_gwbridge  anywhere             anywhere             ctstate RELATED,ESTABLISHED
    0     0 DOCKER     all  --  any    docker_gwbridge  anywhere             anywhere            
    0     0 ACCEPT     all  --  docker_gwbridge !docker_gwbridge  anywhere             anywhere            
    0     0 DROP       all  --  docker_gwbridge docker_gwbridge  anywhere             anywhere            

Chain OUTPUT (policy ACCEPT 140K packets, 39M bytes)
 pkts bytes target     prot opt in     out     source               destination         
```

* `prot` : It denotes the protocol, for instance, tcp, udp.

* `opt` : Special options for that specific rule.

* `in` : Name of input interface via which the packet is received

* `out` : Name of output interface via which the packet will be send

* `source` : Source IP address or Domain Name

* `destination` : Destination IP address or Domain Name
