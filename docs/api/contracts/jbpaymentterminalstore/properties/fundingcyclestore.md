# fundingCycleStore

Contract: [`JBPaymentTerminalStore`](/api/contracts/jbpaymentterminalstore/README.md)​‌

Interface: [`JBPaymentTerminalStore`](/api/interfaces/ijbpaymentterminalstore.md)

**The contract storing all funding cycle configurations.**

# Definition

```solidity
/** 
  @notice 
  The contract storing all funding cycle configurations.
*/
IJBFundingCycleStore public immutable override fundingCycleStore;
```

* The value cannot be changed.
* The resulting view function can be accessed externally by anyone.
* The resulting function overrides a function definition from the [`JBPaymentTerminalStore`](/api/interfaces/ijbpaymentterminalstore.md) interface.
