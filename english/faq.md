# FAQ

<details>
<summary>Q. When I access the website, it shows all 0 yen or "no logs".</summary>

A. Please select "Connect Wallet" in the upper right corner
</details>

<details>
<summary>Q. I deposited ETH. However, the numbers on the UI are not shown and I cannot do CJPY mint.</summary>

A. Please set your wallet's RPC to the default one.
</details>

<details>
<summary>
Q. How secure is the Yamato Protocol?
</summary>
A.　Three main attack vectors in DeFi are 1) Oracle manipulation  2) Flash loan and flash mint and 3) Re-entrancy and Yamato implements protection against these 3 attack vectors.　　

1. Oracle manipulation: Yamato uses ChainLink price feeds for ETH/USD and USD/JPY. ChainLink price feeds are basically immune to arbitrary manipulation, but there may be a slight delay. This would be an attack vector if the prices of the collateral were to rise and fall sharply. To prevent the delay from being exploited, the Yamato Protocol restricts collateral pledging & CJPY borrowing in the same block. Attackers must bet that the next block price feed will also be delayed, introducing uncertainty into the attack and effectively preventing the attack from being executed.


2. Flash Loan and Flash Mint: This is an exploitation technique that uses a large unsecured loan fund to attempt to arbitrarily manipulate assets in the protocol. Because the Yamato Protocol restricts pledging and borrowing in the same block, it is impossible for attackers to use flash loans to create distortions. This is due to the security-first design, but it also has drawbacks. i.e. it is not possible to use services via external contracts, such as DeFiSaver for loan swaps or automatic deleveraging.


3. Re-entry: When using ETH (not WETH) in dApp contracts, arbitrary contracts can be inserted, resulting in malicious movement of funds. Yamato has a protection setting called Reentrancy Guard on all collateral-related contracts, which prevents reentrancy attacks from being executed. We chose to use ETH because the Reentrancy Guard provides the same level of security as well as from a gas efficiency and UX perspective.

</details>