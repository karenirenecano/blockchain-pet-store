# blockchain-pet-store

Pet shop tutorial from the official Truffle Suite
https://www.trufflesuite.com/tutorial

All of the code here came from the truffle box of the tutorial^.

![Alt text](/adopt_petstore.gif?raw=true "Pet store blockchain demo")

1. Install Truffle
    ```
    npm install -g truffle
    ```

2. Install Ganache
    https://www.trufflesuite.com/ganache

3. Code your solidity file and save it under `contracts`

4. Create a migration with a prepended number so that the compiler know how to migrate each migration file in that order.

5. Launch the Ganache UI to get your mnemonic words and use that to import a test account to metamask. **Please ensure that you are on a test network as you will lose your real eth forever.** On the `truffle-config.js`, set the `networks.development`'s `host and port`. The host and port is in Ganache's Accounts tab > RPC Server. You may name the `development` into other name you want, or create a separate `network` for your `production` or `staging` environments.

6. On your Metamask, Setup a custom RPC that points to the local Ganache address & port..

7. Create your tests under the `test` folder.

8. Run your tests. 💡 You don't need to manually compile it. Running the tests will compile it.

    ```
    truffle test
    ```
9. If all are green, you can deploy on you local machine.

    ```
    truffle migrate --compile-all --reset --network development
    ```

    + `migrate` This runs all the migrations
    + `--compile-all` Compiles the contracts into byte code that can be used by JS provider (web3.eth)
    + `--reset` run all migrations from the beginning.
    + `--network`, `development` this is the network you have setup on the `truffle-config.js`

10. Run the local frontend

    ```
    npm run dev
    ```