# WOLF Tokenomics



![](../../.gitbook/assets/en-1129.png)

**WOLF** is a governance token that also rewards its holders with a share of exchange revenues. The token distribution follows a fixed supply, decaying emission model.&#x20;

### Contract&#x20;

| Ticker | Chain                | Contract Address |
| ------ | -------------------- | ---------------- |
| WOLF   | Telos EVM (Chain 40) |                  |

### Emissions

_**There are no pre-sales, private sales or pre-listing allocations of the WOLF token.**_&#x20;

All tokens are distributed according to emission schedule. That means that the team funds and treasury funds are distributed at same pace as our LP farms.&#x20;

We also have an allocation hold out for _future investors._ It means that if WolfSwap were to raise investor funds in the future, these investors would enter _after_ the token launch, and not before.&#x20;

### Revenues

* 0.05% of all trades are paid to xWOLF staking pool.&#x20;
* A share of fees from lending interest and liquidations will also be paid to the xWOLF staking pool. The % will be determined at launch of lending product.&#x20;
* WOLF token holders may stake their WOLF to xWOLF and receive a share of the revenues.&#x20;

### Distribution

All JOE tokens will be emitted according to distribution portion. Team, Treasury and Future Investor funds are emitted at schedule as public distribution to LPs.&#x20;

|                                      | **Distribution** |
| ------------------------------------ | ---------------- |
| **Total supply**                     | 500,000,000      |
| **Months to emit**                   | 30               |
| **Liquidity Providers (LP)**         | 50%              |
| **Treasury**                         | 20%              |
| **Dev Team** (3 month cliff)         | 20%              |
| **Future Investors** (3 month cliff) | 10%              |

![Token Distribution](broken-reference)

![Token Distribution over time](broken-reference)

### Emission Schedule

Below are the emission rates. Token emission will begin 3-July, 2021 and end 3-Jan, 2024.

| Date        | WOLF per sec |
| ----------- | ------------ |
| 3-July 2021 | 30           |
| 3-Aug 2021  | 20           |
| 3-Sep 2021  | 17           |
| 3-Oct 2021  | 13.5         |
| 3-Nov 2021  | 10           |
| 3-Dec 2021  | 9.5          |
| 3-Jan 2022  | 9            |
| 3-Feb 2022  | 8.5          |
| 3-Mar 2022  | 8            |
| 3-Apr 2022  | 7.5          |
| 3-May 2022  | 7            |
| 3-Jun 2022  | 6.5          |
| 3-Jul 2022  | 6            |
| 3-Aug 2022  | 5.5          |
| 3-Sep 2022  | 5            |
| 3-Oct 2022  | 4.5          |
| 3-Nov 2022  | 4            |
| 3-Dec 2022  | 3.5          |
| 3-Jan 2023  | 3            |
| 3-Feb 2023  | 2.5          |
| 3-Mar 2023  | 2            |
| 3-Apr 2023  | 1.5          |
| 3-May 2023  | 1.25         |
| 3-Jun 2023  | 1            |
| 3-Jul 2023  | 0.9          |
| 3-Aug 2023  | 0.8          |
| 3-Sep 2023  | 0.7          |
| 3-Oct 2023  | 0.6          |
| 3-Nov 2023  | 0.5          |
| 3-Dec 2023  | 0.4          |
| 3-Jan 2024  | 0.3          |



## **Emission rate** <a href="#emission-rate" id="emission-rate"></a>

### **Per block**

| **Metric**                                                                | **Emission/block (CAKE)** | **Emission/day (CAKE)** |
| ------------------------------------------------------------------------- | ------------------------: | ----------------------: |
| Emission                                                                  |                        40 |               1,152,000 |
| Burned Weekly [(PID 138)](cake-tokenomics.md#why-is-the-cake-burn-manual) |                    -25.75 |                -787,600 |
| **Effective Emission**                                                    |              **<14.25\*** |           **364,400\*** |

\*Effective Emission is in fact slightly below this amount: an additional 45,000 CAKE per day is diverted from the amount allocated to the lottery, and burned (PID 137 - Details below).

In addition to the above, a dynamic amount of CAKE is also [minted to the Dev address](https://bscscan.com/address/0xceba60280fb0ecd9a5a26a1552b90944770a4a0e#tokentxns) at a rate of 9.09%. This means that if 100 CAKE are harvested, then 9.09 CAKE is minted in addition and sent to the Dev Address.

{% hint style="info" %}
All CAKE minted to the Dev address is burned in the weekly burn and never enters circulation.

As such, we haven't included it in the above emission rate.
{% endhint %}

## Distribution <a href="#distribution" id="distribution"></a>

| Distributed to                | Reward/block (% of emission) | Reward/block (total CAKE) |           Reward/day |
| ----------------------------- | ---------------------------: | ------------------------: | -------------------: |
| Farms and Lottery             |                       10.62% |                      4.25 |     122,400 (approx) |
| of which diverted and burned  |                              |                           |              -46,000 |
| Syrup Pools                   |                          25% |                        10 |     288,000 (approx) |
| **Total Daily CAKE Emission** |                              |                           | **364,400 (approx)** |

## **Other Deflationary Mechanics** <a href="#other-deflationary-mechanics" id="other-deflationary-mechanics"></a>

{% hint style="info" %}
The burning process is currently manual. [View burn transactions here](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82?a=0x000000000000000000000000000000000000dead).
{% endhint %}

As well as the above, CAKE is also burned in the following ways:

* **0.05%** of every trade made on PancakeSwap V2
* **100%** of CAKE sent to the Dev address
* **100%** of CAKE performance fees from IFOs
* **100%** of CAKE spent on Profile Creation and NFT minting
* **100%** of CAKE bid during Farm Auctions
* **20%** of CAKE spent on lottery tickets
* **45,000** CAKE per day (historically assigned to the lottery) (_The CAKE for this is generated by a farm - PID 137)_
* **3%** of every Prediction markets round is used to buy CAKE for burning
* **2%** of every yield harvest in the Auto CAKE Pool
* **2%** of every NFT sale on the NFT Market is used to buy CAKE for burning

## Why is the CAKE burn manual?

To hit the ground running, PancakeSwap launched as an MVP (minimum viable product) with the MasterChef contract emitting 40 CAKE per block. For that reason, the early team didn't add additional functions such as the ability to customize the CAKE minting logic. As migrating to a new MasterChef would require a lot of time and effort, the team opted to reduce CAKE emissions instead through a manual burn process by creating two pools:

* Legacy Lottery Pool (PID - 137) - burned CAKE from the lottery
* Burn Pool (PID - 138) - burned CAKE per block

These pools work similarly to the farms, where the Chefs can adjust the percentage of the 40 CAKE per block allocated to it after each CAKE emission reduction vote.

{% hint style="warning" %}
On the day of the burn, the supply shown on the homepage might suddenly jump by several million CAKE.

Don't worry - **THIS CAKE NEVER ACTUALLY ENTERS CIRCULATION:**
{% endhint %}

This apparent jump is just because of how all the CAKE that's allocated for the burn is stored during the week.

The CAKE sent to both pools PID-137 and PID-138 are harvested before completing the weekly token burns, and this makes the Total Supply shown on the site jumping by \~6M. This is because pending CAKE isn’t registered in the Total Supply until it's harvested on the burn day. Once the token burn transaction is completed, the \~6M is shown in the Burned to Date.

## How to Confirm CAKE Supply for yourself

To confirm that the circulating CAKE supply shown on the PancakeSwap homepage is correct,

1. Head to the CAKE token contract on BscScan and [see how much CAKE is held by the Burn Address.](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82#balances) That's the total amount of CAKE that's been burned (removed from circulation FOREVER, and impossible to ever retrieve).
2. Then, subtract this burned amount from the "Total Supply" that BscScan shows.
3. This gives you the actual CAKE supply.

#### **Read more about CAKE's deflationary mechanics on the next page.** <a href="#read-more-about-cakes-deflationary-mechanics-on-the-next-page" id="read-more-about-cakes-deflationary-mechanics-on-the-next-page"></a>
