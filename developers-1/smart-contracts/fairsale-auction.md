# Fairsale Auction

## Code

Code on github: [https://github.com/cryptonative-ch/mesa-smartcontracts/blob/main/contracts/sales/FairSale.sol](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/main/contracts/sales/FairSale.sol)

### placeOrders\(\)

The investor places a bid at a certain price. One investor can place several order at a different price. At this point it's not clear if he/she will get tokens at the end.

[FairSale.sol\#L205](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/26a59272a7014c41dbb88616b9fa0736ef1a94b8/contracts/sales/FairSale.sol#L205)

### cancelOrders\(\)

A bid can be canceled during the sale. Token are returned to the investor wallet. 

[FairSale.sol\#L258](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/26a59272a7014c41dbb88616b9fa0736ef1a94b8/contracts/sales/FairSale.sol#L258)

### claimFromParticipantOrder\(\)

After the auction is finished, the user can withdraw either his unfilled bid or the bought token.

[FairSale.sol\#L465](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/26a59272a7014c41dbb88616b9fa0736ef1a94b8/contracts/sales/FairSale.sol#L465)

