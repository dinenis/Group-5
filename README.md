# Group 5 Homework
## Homework 1
• Form groups of 3 to 5 students \
• Interact with “HelloWorld.sol” within your group to change message strings and change owners \
• Write a report with each function execution and the transaction hash, if successful, or the revert reason, if failed. 

The transaction hash for the deployment of the HelloWorld contract is: 
0x678bbcc8fe06e6978c25cd972f0357d712f9e5b5245756616f06c0c0cf41b724 

The transaction hash for the deployment of the CountFailures contract is:


The provided code has two Solidity contracts named HelloWorld and CountFailures. 

The HelloWorld contract stores a string text and an address owner, which are set during contract deployment. It has a helloWorld function that is publicly viewable and returns the stored text. The setText function is public, but can only be called by the contract owner, using the onlyOwner modifier. Similarly, the transferOwnership function updates the owner address and can only be called by the contract owner due to the onlyOwner modifier. The onlyOwner modifier checks if the caller of the function is the contract owner before executing the function code.

The CountFailures contract has a counter variable that keeps count of the number of times the fallback function is executed. The fallback function is executed when the contract receives a transaction that does not match any of the defined functions. In this case, it increments the counter variable. The contract also has a receive function that can be used to receive ether.
