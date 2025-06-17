---
description: >-
  Yamato Protocol is a crypto-asset overcollateralized stable coin issuance
  protocol. V1 allows the issuance of CJPY (“Convertible JPY”, a Japanese Yen
  equivalent coin) using ETH as collateral.
---

# Yamato Protocol

[Official site (English)](https://app.yamato.fi/#/?lang=en)

## What is Yamato Protocol？

Yamato Protocol [https://app.yamato.fi/#/?lang=en](https://app.yamato.fi/#/?lang=en) is a decentralized and non-custodial CDP platform developed by DeFiGeek Community Japan [https://defigeek.xyz/en/](https://defigeek.xyz/en/)

CJPY serves as an ETH overcollateralized stablecoin designed to maintain a peg to the Japanese Yen. In the future, the Yamato protocol will expand to encompass various tokens as collateral, and a diverse range of fiat stablecoins will be introduced, initially including USD and EUR pegs.

Dune Analytics Dashboard for Yamato Protocol Statistics\
[https://dune.com/dfgc/yamato](https://dune.com/dfgc/yamato)

DefiLlama Page for Yamato Protocol TVL\
[https://defillama.com/protocol/yamato-protocol](https://defillama.com/protocol/yamato-protocol)

## 1 CJPY ＝ 1 JPY peg mechanism

The CJPY is soft-pegged by **game theory** to be equivalent to 1 JPY.

{% hint style="info" %}
What is **game theory** (mainly Nash equilibrium)?\
The idea is that each side behaves either selfishly or rationally, leading to a targeted equilibrium point (in this case, 1 JPY peg). Incentives and other motivators are needed in the dynamics that always outweigh aggressive (destructive, irrational) behavior.
{% endhint %}

1. The minimum collateral ratio at the time of issuance is 130%, which means that 1CJPY can always be expected to be backed by collateral equal to or greater than 1 JPY.
2. 1CJPY can always be redeemed against collateral equivalent to 1 JPY.

### Force to repeg when the price is less than 1 JPY

* Demand to purchase CJPY to repay or redeem
  * Debt of 1 CJPY can be repaid for less than 1 JPY, which increases the demand for purchases in the market.
  * Since CJPY obtained for less than 1 CJPY can be exchanged for 1 JPY worth of collateral through redemption, demand for arbitrage-oriented purchases will increase.

### Force to repeg when the price is over 1 JPY

* Selling demand from CJPY issue in Yamato
  * 1 CJPY borrowed can be sold in the market for 1 JPY or more and demand for arbitrage-oriented sells will increase.
