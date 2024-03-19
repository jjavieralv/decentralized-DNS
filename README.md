# Decentralized DNS

## Idea

We can use IPFS entries to manage DNS entries.
To do this, we can take advantage of IPNS technology to generate dynamic entries that we can update just like a DNS.
With this, we could resolve addresses (of whatever we want, whether they are IPs, other DNS, addresses...) without the need for a centralized DNS.
Additionally, we could leverage IPNS technology to ensure that this information is correct due to the asymmetric key system on which it is built.


## Security ++

There is a scenario that can be leveraged for some established protocols (OpenVPN or WireGuard).
This is the ability to use the node's private key to encrypt the content of the file, and use the public key, which we have already generated to connect, to decrypt this information. This way, we ensure that the information is publicly accessible, but can only be visible to the people or services we want.
With this, we would have a decentralized DNS system, but completely private at the same time adding another layer of protection.

## The Flow

1 Create the document with the desired content.
2 Encrypt it using the private key.
3 Create a new key for IPFS and register the IPNS CID of the file you have created and encrypted.
4 Once the file is distributed, everyone will be able to access the document since it is distributed on IPFS, but only those with the private key will be able to view it.

This is interesting because you can have as many clients as you want, each with their own public keys, and everyone can access the information.

THE PROBLEM WOULD BE THAT ONCE YOU WANT TO REMOVE A PUBLIC KEY, YOU SHOULD REGENERATE USING A NEW PRIVATE KEY ALL THE REMAINING PUBLIC KEYS AND DISTRIBUTE THEM AGAIN AMONG THE DIFFERENT CLIENTS
