# Que 10: How SSH works?

The way SSH works is by making use of a client-server model to allow for authentication of two remote systems and encryption of the data that passes between them.

An SSH client must initiate an SSH session with an SSH server. Most of the connection setup is conducted by the SSH client. Public key cryptography is used to verify the identity of the SSH server, and then symmetric key encryption and hashing algorithms are used to maintain data transmission in ciphertext. That way, privacy and integrity of data transmission in both directions between the client and server is assured, man-in-the-middle attacks are mitigated.

SSH connection, Two keys are maintained. **Public** and **Private** keys. Public Key are stored in server in `/home/user/.ssh/authorized_keys` and private key is handled by user's ssh-agent to authenticate private key to public key. When user tries to SSH into server, server checks public key in authorized_key file corresponding to user's private key. If keys belongs to that user SSH client let user in.

**The steps involved in creating an SSH session go like this:**

1. Client contacts server to initiate a connection.
2. The server responds by sending the client a public cryptography key.
3. The server negotiates parameters and opens a secure channel for the client.
4. The user, through their client, logs into the server.
