Supply chain & data auditing

1. UML diagrams: Activity, Secuence, State and  Data Model

You can found the UML diagrams in the UML folder.


2. Libraries

I had some issues with the versions of truffle-contract.js and web3 and I had to update it.

I'm using truffle-test-utils for events validation, because I had problems with the examples in the started code with deprecations. I'm usign event assertions like this:
assert.web3Events(result, [{ event: 'Harvested' }]);

I'm usign truffle-hdwallet-provider and the project is published in Rinkeby network.


Main versions:
Node v10.19.0
Truffle v5.4.3
web3@1.2.1 



3. IPFS

Ipfs is not used in this project.

4. The project has 10 unit test:

truffle(develop)> test
Using network 'develop'.


Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.

ganache-cli accounts used here...
accounts[0]  0xf6EcAB62a366525BBf95Fca763E80A00e452EF97 => Contract Owner
accounts[1]  0xdAEC2A7B68A1Dd3f587bb0422Af3Fb88Ef02D0Fd => Farmer
accounts[2]  0x30F05E69Eb1871F1893872Bab9E79313892931cb => Distributor
accounts[3]  0xEc9566C44a2716824dFd4Aa9e4f16924A928CAAF => Retailer
accounts[4]  0x4077CFBcaD3ADC95d43dbb48a1481898E583EAe8 => Consumer


  Contract: SupplyChain
    ✓ Testing smart contract function harvestItem() that allows a farmer to harvest coffee (209ms)
    ✓ Testing smart contract function processItem() that allows a farmer to process coffee (92ms)
    ✓ Testing smart contract function packItem() that allows a farmer to pack coffee (106ms)
    ✓ Testing smart contract function sellItem() that allows a farmer to sell coffee (93ms)
    ✓ Testing smart contract function buyItem() that allows a distributor to buy coffee (201ms)
    ✓ Testing smart contract function shipItem() that allows a distributor to ship coffee (82ms)
    ✓ Testing smart contract function receiveItem() that allows a retailer to mark coffee received (165ms)
    ✓ Testing smart contract function purchaseItem() that allows a consumer to purchase coffee (169ms)
    ✓ Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain (71ms)
    ✓ Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain (42ms)


  10 passing (1s)


5. Smart contracts are deployed in Rinkeby's network.

transaction hash:    0x10667c6d399c14333f822bf342052b68116620ba76e0aa246d9a07f94c7f0c57
contract address:    0x005D27ae834CbFcf1c03Ce3f50b3180903D755ee
account:             0x919c2dA8b72c14087DE1EfebcA3708D8aC9617b4

https://rinkeby.etherscan.io/address/0x005d27ae834cbfcf1c03ce3f50b3180903d755ee
