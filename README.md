# WAXC20 Protocol
TRC20 Protocol base on TRON blockchain writing the string into the memo field of the transaction to achieve this.

Official Twitter:[@WAXC_20_WAXI](https://twitter.com/WAXC_20_WAXI)

## Token Economic
 - Token: WACI
 - Supply: 2100000000
 - limit: 1000

## Method
 - deploy: `data:,{"p":"waxc-20","op":"deploy","tick":"waxi","max":"2100000000","lim":"1000"}`
 - mint: `data:,{"p":"waxc-20","op":"mint","tick":"waxi","amt":"1000"}`
 - transfer: `data:,{"p":"waxc-20","op":"transfer","tick":"waxi","detail":[{"to":"WAX Address","amt":"1000"}]}`

## Deploy txid
https://wax.bloks.io/transaction/2c6299008d58c769a033b2fc2ce4074699d51a9777f61102654d00a86a30347e

## Mint WAXI with mycloudwallet.com
 - Amount: 0.00000001 WAX
 - Address: eosio
 - Memo: data:,{"p":"waxc-20","op":"mint","tick":"waxi","amt":"1000"}

## Idea for developing indexer
1. Recording the block number of deploy inscription.
2. Get all transactions of eosio address.
3. Use the FULL NODE HTTP API to get the `from`,`to`,`memo` field of each waxi, match all mint inscriptions.

## Indexer(TBA)


## FAQ
### Why you need transfer to `eosio` account?
Because the WAX blockchain cannot be transferred to your own address. We decided to transfer to the wax token address on the WAX blockchain.

### Why you need transfer to 0.000001 WAX to eosio address?
Since the WAX blockchain cannot transfer zero value, 0.00000001 WAX is the minimum transfer value.





