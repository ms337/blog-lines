---
layout: page
title: "TimeTokens NFT Project"
category: devproject
---

Conceptualized an NFT project to tokenize the most valuable asset in the world: time.

Still working on it with [Apoorv](https://twitter.com/ApoorvSingal) and [Arth](https://twitter.com/arthgupta). Here are some technical details:


## Time Intervals
- Lowest unit of time we are selling:  1 date
- Split up block chain 
- We can have N tokens for 1 date as follows:
	- Allow 1 token for 1 date to be split in the future some t times. Basically 1 token is actually 2*t unit of resolution.

## Future Splits 
- Think stock splits for dates
- Control at “splitting at the transaction level”. So if you split at t, you allow transactions of 0.5 * 2*t  units of resolution.
- Allow “compound transactions” on our marketplace: allow users to buy or sell D days at once. Allow date transactions on OpenSea etc.


## File Storage
- Infura IPFS API, easy.


## Novel Technical Feature
- Allow users to choose their own picture for a token they buy and allow them to change it

## Centralization Problems
- We have some tricky issues to deal with for the above feature
- How do we allow users to edit token medata without relying on a central server?
- Most NFT projects rely on some backend — that is why rug-pulling happens


## OpenSea and Polygon API Problem

- We were initially planning to use Polygon's PoS to avoid huge gas fees for transactions.
- However, OpenSea does not support Polygon endpoints for `createSellOrder`, etc. See https://github.com/ProjectOpenSea/opensea-js/issues/150
- Perhaps Coinbase NFT?

## Auction Logic

```
semaphore = 20 #Auctions that dont have a bid on them yet
if (no_active_auctions_with_no_bids(wallet_id))) and (has_transaction_history(wallet_id)):
  allowCreatingAuction()
else:
  if semaphore > 0:
      semaphore -=1
      allowCreatingAuction()

  else:  
    "Please wait"
```

If you have any ideas, suggestions, feedback, just reach out. 