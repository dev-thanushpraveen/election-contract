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
