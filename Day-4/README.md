## Que 1:  What are daemon Processes?

A daemon (also known as background processes) is a Linux or UNIX program that runs in the background. Almost all daemons have names that end with the letter "d".

## Que 2: What .d represent after a file?

"d" stands for directory and such a directory is a collection of configuration files which are often fragments that are included in the main configuration file. The point is to compartmentalize configuration concerns to increase maintainability.

## Que 3: What is in the hosts file?

The hosts file stores the hostname and ip address. It contains IP addresses separated by a space and then a domain name.

```
127.0.0.1	localhost
127.0.1.1	knoldus-Vostro-3500

# The following lines are desirable for IPv6 capable hosts
::1     ip6-localhost ip6-loopback
fe00::0 ip6-localnet
ff00::0 ip6-mcastprefix
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
```

## Que 4: What is SCP & what does this command do?

The SCP command or **secure copy allows secure transferring of files in between the local host and the remote host** or between two remote hosts. 

**command**
```bash
scp testfile.txt ubuntu@65.0.108.66:/home/ubuntu
```
## Que 5: How port forwarding works? 

**Port forwarding** is the process of forwarding requests for a specific port to another host, network, or port. As this process modifies the destination of the packet in-flight, it is considered a type of NAT operation. It forward data securely from another client application running on the same computer as a [Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell) (SSH) client

**Command for local port forward**

$ ssh -L local_port:destination_server_ip:remote_port ssh_server_hostname

```bash
ssh -L 5636:65.0.108.66:5464 ubuntu@ec2-65-0-108-66.ap-south-1.compute.amazonaws.com
```

**Command for remote port forward**

```bash
ssh –R 8080:localhost:5534 ubuntu@ec2-65-0-108-66.ap-south-1.compute.amazonaws.com
```
