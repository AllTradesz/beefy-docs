# Understanding Divergence Loss [a.k.a. Impermanent Loss (IL)]

Beefy support often encounters questions on an important but confusing aspect of DeFi that arises from the fundamental innovation UniSwap introduced in 2018 of constant-product liquidity pools which an automated market-making (AMM) smart contract may use to provide decentralized asset swapping. This innovation has reigned since as a foundation of DeFi, and by far most liquidity farms continue to use it today, like PancakeSwap.

The formula behind the basic liquidity pool is simple: an amount of an asset, A, times an equivalently valued amount of an asset, B, equals a constant: 

A * B = K

K is only sort of constant, as it changes whenever liquidity is added or subtracted from the pool, and since trading fees are involved, this happens a bit actually with each swap transaction! However it is useful and valid to simplify in order to isolate the phenomenon of divergence loss. So we zero out trading fees and later withdrawals and deposits, and let the market roll its dice. K will stay constant, no matter fluctuations in the price of a unit of A or B.

Divergence loss arises for liquidity providers whenever the ratio of P<SUB>a</SUB> to P<SUB>b</SUB> changes. Why? Because if the liquidity provider had not added to the pool, she would have her A and B assets in the same amounts (not value) in her wallet. Instead, she now has LP token representing her share of the pool, and if she were to withdraw her share, the amounts of A and B she'd receive will _differ_ from what she originally deposited. While the product of their respective prices P<SUB>a</SUB> and P<SUB>b</SUB> will still equal K, the sum of their values will be *less* than if she had simply HODLed instead of deposited. Again, why does this happen, this loss? It happens because, surprise, everything involved in this AMM game is zero-sum! Someone has to push the liquidity pool to balance to reflect market-wide pricing of its assets A & B. Enter arbitrageurs, who play off of market mispricings. These actors eke out a gain with each successful buy-sell performed, and their gain is your loss as the liquidity provider.

It's all very mathematical. Indeed a wonderful, universal chart speaks a thousand words.

