# Que 1: How many tables are there in iptables?

**There are 5 tables in iptables.**

1. `Filter Table` : The filter table is used to make decisions about whether to let a packet continue to its intended destination or to deny its request. Its is default iptable.

2. `NAT table` : The nat table is used to implement network address translation rules. As packets enter the network stack, rules in this table will determine whether and how to modify the packet’s source or destination addresses in order to impact the way that the packet and any response traffic are routed.

3. `Mangle Table` : The mangle table is used to alter the IP headers of the packet in various ways. For instance, you can adjust the TTL (Time to Live) value of a packet, either lengthening or shortening the number of valid network hops the packet can sustain. Other IP headers can be altered in similar ways.

4. `Raw Table` : Its only purpose is to provide a mechanism for marking packets in order to opt-out of connection tracking.

5. `Security Table` : The security table is used to set internal SELinux security context marks on packets, which will affect how SELinux or other systems that can interpret SELinux security contexts handle the packets. These marks can be applied on a per-packet or per-connection basis.
