---
description: Manages and normalizes price feeds.
---

# JBPrices

## Overview

### [Code](https://github.com/jbx-protocol/juice-contracts-v2/blob/main/contracts/JBPrices.sol)

### **Addresses**

Ethereum mainnet: _Not yet deployed_

### **Interfaces**

| Name                                             | Description                                                                                                                              |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [**`IJBPrices`**](/api/interfaces/ijbprices.md) | General interface for the methods in this contract that interact with the blockchain's state according to the protocol's rules. |

### **Inheritance**

| Contract                                                                  | Description                                                                                                                              |
| ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [**`Ownable`**](https://docs.openzeppelin.com/contracts/4.x/api/access#Ownable) | Includes convenience functionality for checking a message sender's permissions before executing certain transactions. |

## Constructor

```solidity
constructor(address _owner) {
  // Transfer the ownership.
  transferOwnership(_owner);
}
```

* **Arguments:**
  * `_owner` is the address that will own the contract.
## Events

| Name                               | Data                                                                                                                                                                                    |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**`AddFeed`**](/api/contracts/jbprices/events/addfeed.md) | <ul><li><code>uint256 indexed currency</code></li><li><code>uint256 indexed base</code></li><li><code>[IJBPriceFeed](/api/interfaces/ijbpricefeed.md) feed</code></li></ul> |

## Properties

| Function                                                          | Definition                                                                                                                                                                                                |
| ----------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**`feedFor`**](/api/contracts/jbprices/properties/feedfor.md)                            | <p><strong>Params</strong></p><ul><li><code>uint256 _currency</code></li><li><code>uint256 _base</code></li></ul><p><strong>Returns</strong></p><ul><li><code>[IJBPriceFeed](/api/interfaces/ijbpricefeed.md) feed</code></li></ul> |

## Read

| Function                                 | Definition                                                                                                                                                                                   |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**`priceFor`**](read/pricefor.md) | <p><strong>Params</strong></p><ul><li><code>uint256 _currency</code></li><li><code>uint256 _base</code></li><li><code>uint256 _decimals</code></li></ul><p><strong>Returns</strong></p><ul><li><code>uint256 price</code></li></ul> |

## Write

| Function                             | Definition                                                                                                                                                                                                                               |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**`addFeedFor`**](/api/contracts/jbprices/write/addfeed.md) | <p><strong>Traits</strong></p><ul><li><code>onlyOwner</code></li></ul><p><strong>Params</strong></p><ul><li><code>uint256 _currency</code></li><li><code>uint256 _base</code></li><li><code>[IJBPriceFeed](/api/interfaces/ijbpricefeed.md) feed</code></li></ul> |
