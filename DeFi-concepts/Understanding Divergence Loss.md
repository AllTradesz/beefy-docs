# Understanding Divergence Loss [a.k.a. Impermanent Loss (IL)]

Beefy support often encounters questions on an important but confusing aspect of DeFi that arises from the fundamental innovation UniSwap introduced in 2018 of algorithmic liquidity pools which an automated market-making (AMM) smart contract may use to provide decentralized asset swapping. This innovation has reigned as the foundation of DeFi since, by far the most liquidity farms continue to use it today.

The algorithm behind the basic liquidity pool is simple: price of asset X times price of asset Y equals a constant.

  P<SUB>x</SUB> * P<SUB>y</SUB> = K

The constant K is set at the time of the liquidity pool's first provisioning, and it doesn't change.

Divergence loss arises for liquidity providers whenever the ratio of P<SUB>x</SUB> to P<SUB>y</SUB> changes. Why? Because if the liquidity provider had not added to the pool, she would still have her X and Y assets in the same amounts (not value) in her wallet. Instead, she now has LP token representing her share of the pool, and if she were to withdraw her share, the amounts of X and Y will differ from what she originally deposited. While the product of their respective prices P<SUB>x</SUB> and P<SUB>y</SUB> will still equal K, the sum of their values will be *less* than if the amounts hadn't changed, i.e. if she had HODLed instead of deposited. Again, why, or, better, How does this happen? It happens because everything involved in this AMM game is zero-sum
