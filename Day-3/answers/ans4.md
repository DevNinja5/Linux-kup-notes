# Que 4: What type of rules we can add to the iptables?

The iptables rules can be specified with 3 blocks, which are used for specific purpose (called `Chains`):

- **INPUT** : All packets destined for the host computer.
- **OUTPUT** : All packets originating from the host computer.
- **FORWARD** : All packets neither destined for nor originating from the host computer, but passing through (routed by) the host computer. 

We can perform different actions on different rules:
- **ACCEPT** : Accepts the packages
- **DROP** : Deny the packages silently
- **REJECT** : Rejects ackages and informs or print messages.
