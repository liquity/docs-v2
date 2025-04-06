# BOLD & Earn

### What is BOLD?

BOLD is the USD-pegged stablecoin issued in Liquity V2. It’s fully decentralized, overcollateralized and backed only by WETH, wstETH and rETH.

In contrast to most of its competitors, BOLD is a resilient stablecoin by design:&#x20;

* only backed by crypto assets (no real world assets or custody by centralized players)
* not subject to collateral changes and protocol upgrades (immutable)
* directly redeemable (always convertible in a fast and liquid way)

### What are BOLD's main benefits compared to other stablecoins?

* BOLD uses only the most decentralized assets as collateral - WETH, wstETH and rETH&#x20;
* It is always redeemable for the underlying assets, meaning you can always swap it as if worth $1, for the collateral backing it
* The contracts used to issue BOLD are immutable, not allowing any changes and significantly reducing attack vectors
* BOLD has native incentives via Protocol Incentivized Liquidity ([PIL](lqty-staking.md#docs-internal-guid-8a7939ae-7fff-d87a-a798-f657d5fd8501)) directed by governance, ensuring that there will always be sufficient liquidity to handle transactions

### What is BOLD’s peg mechanism?

Liquity V2's market-driven monetary policy through user-set interest rates enables BOLD's peg to dynamically respond to situations where the token is above or below $1.

When BOLD trades above $1, borrowers tend to reduce their rates due to lower [redemption](redemptions-and-delegation.md#what-are-redemptions) risk, making borrowing more and holding BOLD less attractive. This helps correct the price downwards.

In contrast, when BOLD trades below $1, arbitrageurs will initiate redemptions to restore the peg. Moreover, borrowers' exposure to redemption risk prompts them to increase interest rates, boosting demand for BOLD (and Earn deposits) and pushing its price upward.

<figure><img src="../.gitbook/assets/light - BOLD peg mechanism.png" alt=""><figcaption></figcaption></figure>

### How can I earn with Liquity v2?

* Stability Pool deposits (Earn): Earn protocol revenue by depositing BOLD into the various Stability Pools.
* Protocol Incentivized Liquidity (PIL): Supply liquidity for BOLD onto the incentivized external DEXes.&#x20;
* Stake LQTY: Receive protocol revenue from Liquity V1 while accruing voting power over liquidity incentives by staking LQTY. On top of directing revenue and receiving V1 fees, LQTY stakers can potentially receive bribes (subject to governance vote) from third parties as an added bonus.

### Where does the yield for Earn come from?

The yield comes from two sources:

* **Interest payments:** Each borrow-market funnels 75% of the of its revenue to its Stability Pool depositors (Earners). This is paid out in BOLD.
* &#x20;**Liquidation gains:** Your BOLD will be used to liquidate under-collateralized loans, effectively buying their collateral with a \~5% discount. This is paid out in (staked) ETH.

All the yield is fully sustainable, scalable and “real”, with no token emissions and lockups.

### Is there a lockup period?  <a href="#docs-internal-guid-e33469f8-7fff-3873-3b78-742f370cf298" id="docs-internal-guid-e33469f8-7fff-3873-3b78-742f370cf298"></a>

There is no lockup period. Users are free to withdraw their BOLD deposits whenever they want.&#x20;

### What is the estimated yield on Earn? <a href="#docs-internal-guid-9adfe211-7fff-6cdc-ba63-258b45131fbf" id="docs-internal-guid-9adfe211-7fff-6cdc-ba63-258b45131fbf"></a>

The yield is a representation of the rates borrowers are paying. Since 75% of the borrowers’ interest payments go to Earn, the effective yield can exceed the average interest rate paid in a borrow market if less than 75% of the BOLD supply is deposited to the respective Stability Pool. This yield amplification sets Liquity V2 apart from competitors and money markets where lending rates cannot be higher than borrow rates.

Check historic rates [here](https://dune.com/liquity/liquity-v2#interest-rates).

### Why are there multiple Stability Pools?

The goals are to:

* Establish separate borrow markets for different collateral assets with their own market driven interest rates, using the Stability Pool backing to dynamically split redemptions across the available collaterals (link to “Redemption”).&#x20;
* Compartmentalize the risks as much as possible when depositing to the respective Stability Pools (Earn) by giving the depositors control over which collateral assets they want exposure to in case of liquidations.

### How have Stability Pools evolved from V1 to V2?

In V2, the concept of Stability Pools is expanded to accommodate multiple Liquid Staking Tokens (LSTs) and ETH as collateral, keeping the interest revenue and liquidations proceeds inside the respective borrow market (collateral). Each collateral asset thus has its own Stability Pool to distribute yield to BOLD depositors.

Additionally, user-set interest rates in V2 influence the yield dynamics for  Stability Pools depositors (Earn) as the yield is now fully sustainable coming from user-set interest rates (in BOLD) rather than token emissions.

### How do risks differ for the different Stability Pools?

Users can deposit their stablecoins into the Stability Pool of their choice, aligning with their risk preference and the types of collateral they're comfortable being exposed to. By selecting pools associated with specific LSTs or ETH, participants can tailor their risk exposure and potential reward profile.

By offering separate pools for different collateral types, the system allows users to choose their exposure based on the perceived risk and potential returns of each LST or ETH. This compartmentalization helps manage systemic risk, ensuring that impacts from liquidations in one asset class don't disproportionately affect the entire ecosystem.

It is important to note that all BOLD holders including depositors still remain dependent on BOLD to keep its peg, remaining exposed to both all LSTs and ETH.\
