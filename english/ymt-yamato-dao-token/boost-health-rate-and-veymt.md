# Boost: Health Rate & veYMT

Yamato offers two type of boosts.&#x20;

The veYMT boost multiplier will be implemented in v1.5.&#x20;

The health rate boost multiplier will be applied from v1 launch, with retroactive YMT allocation (one year of linear vesting) at v1.5 launch.&#x20;

Each boost multiplier can be up to 2.5x, for a total boost of max 6.25x.

## **veYMT boost multiplier**

Following formula is used to calcurate score then veYMT boost multiplier is assigned per table.

$$
\rm{
    score = \frac{USERveYMT}{TOTALveYMT} / \frac{USERCJPYminted}{TOTALCJPYminted} * 2.5
}
$$

$$
veYMTboostmultiplier = \left\{
\begin{array}{ll}
    2.5 & (\mathrm{score} \gt 2.5) \\
    \mathrm{score} & (1 \leq \mathrm{score} \leq 2.5) \\
    1 & (\mathrm{score} \lt 1) \\
\end{array}
\right .
$$

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>Boost multiplier: veYMT share &#x26; CJPY share</p></figcaption></figure>



## **Health Rate boost multiplier**

The boost is applied by keeping the Yamato Pledge health rate high.&#x20;

The relationship between the health rate and the multiplier is shown in the table below.

| Health Rate(%) | multiplier |
| :------------: | :--------: |
|  Less than 130 |      0     |
|      130\~     |      1     |
|      150\~     |     1.5    |
|      200\~     |      2     |
|      250\~     |     2.5    |

## Total boost multiplier

veYMT boost multiplier（1～2.5）\* Health Rate boost multiplier（0～2.5） 　→　0 , 1～6.25&#x20;



User Debt amount x Total boost multiplier → Distribution score → Accrued per block&#x20;

User distribution score / Total distribution score → User reward share&#x20;

User reward share × YMT reward per block → User reward



YMT reward per block = User Reward Distribution Ratio (by CJPY, CUSD, CEUR, etc.) \* Annual Reward Distribution Speed / Number of Blocks per Year (2,628,000 blocks)

