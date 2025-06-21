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

## User Reward Calculation

veYMT boost score (1 to 2.5) × Collateral Ratio boost score (0 to 2.5) → Total boost score (0 or 1 to 6.25)  
\
Borrowing amount × Total boost score → Distribution score → Accumulated per block

Your distribution score / Total distribution score → Allocation rate

Allocation rate × YMT per block → User reward

{% hint style="info" %}
**YMT per block** is calculated as:  
(User reward distribution ratio for each asset type — e.g., CJPY, CUSD, CEUR, etc.) × Annual distribution speed per block / Number of blocks per year (2,628,000 blocks)
{% endhint %}

{% hint style="info" %}
**Checkpoints and Update Triggers**  
\
A *checkpoint* is the timing when the distribution score — calculated as:  
Borrowing amount × veYMT boost × Collateral Ratio boost — is updated and recorded.  
\
Checkpoints and distribution scores are updated when the following actions occur:  
1. CJPY borrowing or repayment  
2. Collateral deposit or withdrawal  
3. Redemption or repayment  
\
※ For redemption or repayment, only the Pledge being redeemed or repaid will have its distribution score and checkpoint updated.  
※ The account that **executes** the redemption or repayment transaction will not have its score updated.
{% endhint %}

{% hint style="info" %}
**User Reward Distribution Methods by Period**  
\
The first YMT allocation accumulates distribution scores on a weekly basis starting from May 26, 2025,  
and the total allocation for that 9-week period will be executed on July 25, 2025.  
Assuming all Pledges have the same score, up to a 10× difference in allocation may occur,  
so it is recommended to acquire a checkpoint as early as possible.  
\
From the second YMT allocation onward, distribution scores are checked every Thursday at 9:00 a.m. (JST),  
and the allocation for that week is finalized. Rewards can be claimed immediately.  
\
- 1st YMT allocation: July 25, 2025 (exceptionally on a Friday)  
- 2nd YMT allocation: July 31, 2025 (Thursday, 9:00 a.m.)  
- 3rd YMT allocation: August 7, 2025 (Thursday, 9:00 a.m.)  
- Weekly allocations continue every Thursday at 9:00 a.m. thereafter
{% endhint %}