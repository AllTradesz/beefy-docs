# Understanding Divergence Loss [a.k.a. Impermanent Loss (IL)]

Beefy support often gets questions on an important but confusing aspect of DeFi that arises from the innovation UniSwap introduced in 2018 of constant-product liquidity pools which an automated market-making (AMM) smart contract may use to provide decentralized asset swapping. This innovation has reigned since as a foundation of DeFi. By far most liquidity farms continue to use it today, like PancakeSwap.

The formula behind the basic liquidity pool is simple: an amount of an asset, A, times an _equivalently valued_ amount of an asset, B, equals a constant: 

A * B = K

K is only sort of constant, as it changes whenever liquidity is added or subtracted from the pool, and since trading fees are involved, an addition happens a bit actually with each swap transaction! Yet it is useful and valid to simplify in order to isolate the phenomenon of divergence loss. So we will zero out trading fees and withdrawals and deposits, and let the market endlessly roll its dice. K will stay constant, no matter fluctuations in the price of a unit of A or B.

Divergence loss arises for liquidity providers as soon as the original price ratio of A to B changes. That is once PA<SUB>0</SUB>/PB<SUB>0</SUB> != PA<SUB>t</SUB>/PB<SUB>t</SUB>. If the ratio continues to change in the same direction up or down, the loss increases, and if it does the opposite and moves toward the original ration, the loss decreases. What is there loss? Well, it's because if the liquidity provider had not added to the pool, she would have instead her A and B assets in the original amounts (not value) in her wallet, HODLing. But as a liquidity provider, she only has LP token representing her share of the pool, and if she were to withdraw her share, the amounts of A and B she'd receive back will _differ_ from what she originally deposited. While the product of their respective amounts A * B will still equal K, the sum of their values will be *less* than if she had simply HODLed. But again you ask, why does this happen, this loss? It happens because, surprise, everything involved in this AMM game is zero-sum! Someone has to push the liquidity pool to balance to reflect market-wide pricing of its assets A & B. Enter arbitrageurs, who play off of market mispricings. These actors eke out a gain with each successful buy-sell performed, and their gain is your loss as the liquidity provider.

It's all very mathematical. Indeed a wonderful, universal chart speaks a thousand words.

