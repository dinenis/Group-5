# Group 5 Homework
## Homework 1
### Assignment
• Form groups of 3 to 5 students \
• Interact with “HelloWorld.sol” within your group to change message strings and change owners \
• Write a report with each function execution and the transaction hash, if successful, or the revert reason, if failed.

### Results

The provided code has two Solidity contracts named HelloWorld and CountFailures. 

The HelloWorld contract stores a string text and an address owner, which are set during contract deployment. It has a helloWorld function that is publicly viewable and returns the stored text. The setText function is public, but can only be called by the contract owner, using the onlyOwner modifier. Similarly, the transferOwnership function updates the owner address and can only be called by the contract owner due to the onlyOwner modifier. The onlyOwner modifier checks if the caller of the function is the contract owner before executing the function code.

The CountFailures contract has a counter variable that keeps count of the number of times the fallback function is executed. The fallback function is executed when the contract receives a transaction that does not match any of the defined functions. In this case, it increments the counter variable. The contract also has a receive function that can be used to receive ether.

We compiled and Deployed the Hello World contract in Hello World.sol

Transaction for Contract Deployment
https://goerli.etherscan.io/tx/0x9fb7142664c2f5189a9d53c002eacda6386838f14953392449b36a3eed00073c

The address of the new contract we have created is: 0xaf5ec484addf721ae156ba9fccd5412a0068b3ee

We can view the contract and all of our tests here:
https://goerli.etherscan.io/address/0xaf5ec484addf721ae156ba9fccd5412a0068b3ee

We tested the setText function. We changed the string to each of the following. 

Test 1: Hi Group 5
https://goerli.etherscan.io/tx/0xd5a0992a8657905d437c81fcd1b572ee97789d5f270e82cc5b6e28d283e67891

Test 2: null
https://goerli.etherscan.io/tx/0x49b269e5192c4d20bbe67a0d2d1b89092c48b5ad43f3c76cd715483539d10781

Test 3: asfkjhasfghasfglhasdtlieirtowutuweituweotpweutpweuitpweutpuwepytupweuypweruypwue
https://goerli.etherscan.io/tx/0xfd1539949bfe46d9b4dd4b19063b5f06b188f62610050fd1b0587a6268357097

Test 4: Estado de SÃO PAULO Coçar
https://goerli.etherscan.io/tx/0xcc6f6b4e21663654632e53e4c8da10b0a23811e62a2fc952bc4a0ea042ffb26c

Test 5: Estado de S\xC3\x83O PAULO Co\xC3\xA7ar
https://goerli.etherscan.io/tx/0xdb4197462ef0b520d388fe96fa2627e1352050c03331d0e2f2f4e038631ddfbf

We can view the state changes in the contract itself. 
https://goerli.etherscan.io/tx/0xcc6f6b4e21663654632e53e4c8da10b0a23811e62a2fc952bc4a0ea042ffb26c#statechange

We then test the change ownership functions.
https://goerli.etherscan.io/tx/0x4d4c3b33dc003b7a4c4516920122c650559480fbbfacdd1dc834bbf29593b117

We then change the text. This fails as I am no longer the owner. 
https://goerli.etherscan.io/tx/0x2ee032bcc928aff2150e79a34cc46fa56d8094e316814c9ec636c4b09b07f605





