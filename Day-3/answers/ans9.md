# Que 9: What are public & private keys?

> **Key Pairs - Public and Private** are used in SSH connection to make authenticate the user and to maintain secure connection. To generate key-pairs in linux, use command `ssh-keygen -f key-name`

* `Public Key` is copied to the SSH server(s). Once an SSH server receives a public key from a user and considers the key trustworthy, the server marks the key as authorized in its `/home/user/.ssh/authorized_keys` file. Such keys are called authorized keys. After adding **public key** to authorized_keys file, user with corresponding private key can SSH into the server or CVM.

* `Private Key` that remains (only) with the user. The possession of this key is proof of the user's identity. Only a user in possession of a private key that corresponds to the public key at the server will be able to authenticate successfully. The private keys need to be stored and handled carefully, and no copies of the private key should be distributed. The private keys used for user authentication are called identity keys.
