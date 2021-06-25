# Fixed Price Sale

## Code

Code on github: [FixedPriceSale.sol](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/main/contracts/sales/FixedPriceSale.sol)

For a FixedPrice Sale there are this 3 function calls to be made from the investor facing interface.

### buyTokens\(\)

If an investor buys a token, he makes an order but does not get the token back yet. Only after the sale has closed and the threshold is reached, the investor will be able to claim the token. If the threshold is not reached, the invested amount has to be withdrawn afterwards.

[FixedPriceSale.sol\#L171](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/26a59272a7014c41dbb88616b9fa0736ef1a94b8/contracts/sales/FixedPriceSale.sol#L171)

### claimTokens\(\)

This is the function users call to claim the bought token after the sale has finished.

[FixedPriceSale.sol\#L23](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/26a59272a7014c41dbb88616b9fa0736ef1a94b8/contracts/sales/FixedPriceSale.sol#L23)

### releaseTokens\(\)

This is the function users call to claim to get the invested token back if the threshold has not been hit.

[FixedPriceSale.sol\#L208](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/26a59272a7014c41dbb88616b9fa0736ef1a94b8/contracts/sales/FixedPriceSale.sol#L208)

