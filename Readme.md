
Dapp University
---------------

- [Javascript for Blockchain](https://www.youtube.com/watch?v=itUrxH-rksc&feature=youtu.be)

Code: https://github.com/dappuniversity/web...
* [02:39:57] Web3.js #1
* [03:00:22] Web3.js #2
* [03:20:13] Web3.js #3
* [03:32:45] Web3.js #4
* [03:54:09] Web3.js #5
* [04:16:20] Web3.js #6
* [04:34:47] Web3.js #7
* [04:49:22] Web3.js #8


## Let's get started: 
##### Useful docs&links we should be aware before! 
- [https://web3js.readthedocs.io/en/v1.2.1/](https://web3js.readthedocs.io/en/v1.2.1/)
- [https://github.com/ethereum/web3.js](https://github.com/ethereum/web3.js)
- [http://iotbl.blogspot.com/2017/03/ethereum-and-blockchain-2.html](http://iotbl.blogspot.com/2017/03/ethereum-and-blockchain-2.html)
- [https://en.wikipedia.org/wiki/JSON-RPC](https://en.wikipedia.org/wiki/JSON-RPC)
- [https://infura.io/](https://infura.io/)

## Next step:
-  Check node `node -v` and web3 version `npm ls web3`
-  Initialize the project `npm init` 
-  Install modules `npm install`
-  Install web3 `npm install web3`
-  If you are getting an " web3 module not found" or similar error, 
   try running `npm install --production windows-build-tools`, 
   then `npm install web3`, and finally, `npm audit fix` 
## Web3.js #1 
  $ node
  > var Web3 = require('web3')
  undefined
  
  > Web3
  -// a set of web3 methods will appear
  
  -// get an API key from Infura
  > var url = 'https://mainnet.infura.io/v3/ea9dd948eceb46c888515813a41924ce'
  undefined
  
  >var web3 = new Web3(url)
  undefined
 
  >web3
  // a set of web3 methods will appear
 
  //use Etherscan.io to find an account 
  > var address = '0xBE0eB53F46cd790Cd13851d5EFf43D12404d33E8'  
  undefined
  
  //get account balance
  > web3.eth.getBalance(address, (err, bal) => { balance = bal })
  > balance
  '1985015119547778877280409'
  
  //convert it to ETH
  > web3.utils.fromWei(balance,'ether')
  '1985015.119547778877280409'
  
  //create an account. This is not a SECURE method
   web3.eth.accounts.create()

## Web3.js #2
   $ node
   > var Web3 = require('web3')
   undefined
   var web3 = new Web3('https://mainnet.infura.io/v3/ea9dd948eceb46c888515813a41924ce')
   web3
   
   //copy ABI from any coin on etherscan.io
   // e.g. from https://etherscan.io/address/0xd26114cd6EE289AccF82350c8d8487fedB8A0C07#code
   var abi =  //paste ABI here ⚠️
 
   // copy contract`s address
   > var contractAddress = '0xd26114cd6EE289AccF82350c8d8487fedB8A0C07'
   > contractAddress
   var contract = new web3/eth.contract(abi, contractAddress)
   > contract
   
   contract.methods.name().call((err, result) => {console.log(result) })
   contract.methods.symbol().call((err, result) => {console.log(result) })
   contract.methods.totalSupply().call((err, result) => {console.log(result) })
   contract.methods.mintingFinished().call((err, result) => {console.log(result) })
   
   //find an address of token holder from etherscan.io
   var accountAddress ='0xd26114cd6EE289AccF82350c8d8487fedB8A0C07'
   contract.methods.balanceOf(accountAddress).call((err, result) => {console.log(result) })
   
   

FYI I ended here [https://youtu.be/itUrxH-rksc?t=10037](https://youtu.be/itUrxH-rksc?t=10037)
    I ended here: https://youtu.be/itUrxH-rksc?t=12012


