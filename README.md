# Deployed GSN contracts.

A list officlally deployed GSN network for various networks.

## How to use these entries:

### Client

A client only needs to know its paymaster. on testnet, you can use the deployed "accept-everything" paymasters.
On real network, you must deploy your own paymaster.

### RelayRecipient contracts

These are the actual contracts o


#### NOTES:
- paymasters are the default "accept-everything" paymaster. these are deployed ONLY on testnets, as they can easily be abused and depleted. If you use such a paymaster and you get an error that it has no funds, simply send test eth to its address to replenish it...

- when creating your own paymaster, make sure to use the official forwarder.
- likewise, when creating your target contract, make sure it uses the forwarder for your network. This way, users can access your contract either through the standard or through your paymasters.

- When bringing up a relayer, the only address you should use is the VersionRegistry. the RelayHub is registered in the registry with id "hub". This mechanism will allow us in the future to upgrade the relayhub, while keeping relayers working intact.
  It IS possible for a relayer to work directly with the RelayHub, but then it can't be easily upgraded.

