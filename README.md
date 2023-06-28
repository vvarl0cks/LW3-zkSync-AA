# Custom Account Abstraction (AA) Tutorial

In this lesson, we're gonna be building and deploying a 2-of-2 multi-signature account via a factory contract, which is basically a contract that executes instructions only after both of its owners attest their signature. We'll also test it by sending a transaction.   

-Code for the "Account abstraction" tutorial from the [zkSync v2 documentation](https://v2-docs.zksync.io/dev/).
-You can find a full step-by-step guide to build this project [in this article](https://v2-docs.zksync.io/dev/tutorials/custom-aa-tutorial.html#prerequisite).
-Portal Faucet [ZkSync Era Goerli Portal](https://goerli.portal.zksync.io/faucet)

## Installation and compilation

You need Node.js and Yarn.

Install all dependencies with `yarn`.

Compile contracts with `yarn hardhat compile`

## Deployment and usage

To run the scripts to deploy and execute the contracts, use the `zksync-deploy` command:

- `yarn hardhat deploy-zksync --script deploy-factory.ts`: deploys the factory contract
- `yarn hardhat deploy-zksync --script deploy-multisig.ts`: deploys a multisig wallet and executes a transaction.

# Deploy

```shell
gitpod /workspace/LW3-zkSync-AA (main) $ yarn hardhat deploy-zksync --script deploy-factory.ts
yarn run v1.22.19
$ /workspace/LW3-zkSync-AA/node_modules/.bin/hardhat deploy-zksync --script deploy-factory.ts
AA factory address: 0xC23929abb6369Adf608f33F72FdDA4028F4d6F53
Done in 6.16s.
```

```shell
gitpod /workspace/LW3-zkSync-AA (main) $ yarn hardhat deploy-zksync --script deploy-multisig.ts
yarn run v1.22.19
$ /workspace/LW3-zkSync-AA/node_modules/.bin/hardhat deploy-zksync --script deploy-multisig.ts
Multisig account deployed on address 0x53EE0907bc107954D895Cd5a35Ee04057462480c
Sending funds to multisig account
Multisig account balance is 8000000000000000
The multisig's nonce before the first tx is 0
The multisig's nonce after the first tx is 1
Multisig account balance is now 7948379500000000
Done in 11.48s.
```
## Support

Check out the [common errors section in the tutorial](https://v2-docs.zksync.io/dev/tutorials/custom-paymaster-tutorial.html#prerequisite), open an issue, or [contact us on Discord](https://discord.com/invite/px2aR7w).