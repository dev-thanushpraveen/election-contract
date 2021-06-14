# Create a root project using truffle

_Step 1_: Run ganache and run

```
truffle unbox pet-shop
```

_Step 2_: Write your own contract:

```
pragma solidity ^0.8.1;

contract Election {
    // Store candidate
    // Read candidate
    // Contructor
    string public candidate;

    constructor() {
        candidate = "Cand1";
    }
}

```

_Step 3_: create new migration file for Election contract named **2_deploy_contracts.js**

```
var Election = artifacts.require("./Election.sol");

module.exports = function (deployer) {
  deployer.deploy(Election);
};

```

_Step 4_: Run the migration

```
truffle migrate
```

_Step 5_: Get the deployed contract details by running **truffle config** and run **Election.deployed().then(function(instance){app = instance})**. Now you can get contract address by running **app.address** and get candidate by running **app.candidate()**

# Listing the details

_Step 1_:
