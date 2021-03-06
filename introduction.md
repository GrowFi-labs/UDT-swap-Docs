UDTswap Feature
---------------
* Token pairs are not limited.
* Trade any UDT to any UDT direct swap support. 
* Automated pricing using Constant Product (x * y = k) market maker formula.
* Anyone on-chain liquidity pool can participate.
* Supports CKB and any UDT based pools.
* Supports multiple pools for same CKB and UDT pairs.
* Supports multiple swaps for different pools.
* Liquidity providers earn exchange fees.
* Front running can be prevented.
* Protocol protection fees.

Resources
---------
* Website
* Github
* Twitter
* Discord

## Introduction
UDTswap is an automated exchange protocol using multiple liquidity pool economy on Nervos. UDTswap is a decentralized exchange that replaces order books with an on-chain liquidity pool. Any liquidity pool can be created. In addition, existing automated market maker (AMM) protocols can set a base currency and create a token pair, but there is no limit to the base currency in UDT swap. When liquidity is added to the liquidity pool, the price is automatically formed through the constant product market maker mechanism (x * y = k). Liquidity pool providers will earn exchange fees (0.3% incentives) incurred in the corresponding token pair swap.

Each liquidity pool has two UDTs. To deposit in a liquidity pool, you deposit the equivalent value of a UDT pair. The “Liquidity token (UDT)” of the pool is issued to all liquidity pool providers and is used to verify the provider's liquidity pool contribution. In addition, Liquidity tokens are burned in proportion to the withdrawal of funds deposited in the liquidity pool.
At UDTswap, anyone can list tokens, and UDT as well as CKB can be listed as a base currency. For example, you can make a CKB/BTC pair that is a CKB base currency, but you can also create a BTC/USDT pair as the BTC base currency. Users can only swap if there is a liquidity pool for that token pair.

Unlike traditional decentralized exchanges using AMM models, which operate as a single liquidity pool, UDTswap supports multiple pools. For example, there can be multiple liquidity pools in CKB / USDT token pairs (EX:CKB / USDT Pool A, Pool B, Pool C etc ...)

As one live cell per liquidity pool, if a user tries to add / remove / swap from that pool, other users will not be able to use the pool until the status is updated. Since this can cause pool occupancy problems, UDTswap can solve the problem by supporting multiple pools and protection fees.

The protocol protection fees are set to 61 CKB. Users must pay protocol protection fees when using UDTswap. Subsequent figures can be changed through the governance process. The protocol protection fees are used not only to increase the security of UDTswap, but also to build a continuously growing open finance infrastructure.
UDTswap supports not only CKB but also UDT for basic assets to expand the Nervos and longtail asset (UDT) ecosystem in the future. Also, the liquidity pool of most existing swap models only supports a single pool, but UDTswap supports multiple pools. As a result, UDTswap offers more economic opportunities for liquidity providers (LP).

#### Front running
UDTswap is cell model. If someone wants to use UDTswap, he must use the pool cell as input. And if someone catches the transaction and send another transaction faster, then the first transaction can not be mined because the transaction is not using live pool cell.
