# Understanding Divergence Loss [a.k.a. Impermanent Loss (IL)]

Beefy support often encounters questions on an important but confusing aspect of DeFi that arises from the fundamental innovation UniSwap introduced in 2018 of algorithmic liquidity pools which an automated market-making smart contract may use to provide decentralized asset swapping. This innovation has reigned as the foundation of DeFi since, by far the most liquidity farms continue to use it today.

The algorithm behind the basic liquidity pool is simple: price of asset X times price of asset Y equals a constant.

  P<SUB>x</SUB> * P<SUB>y</SUB> = K

The constant K is set at the time of the liquidity pool's first provisioning, and it doesn't change. 
