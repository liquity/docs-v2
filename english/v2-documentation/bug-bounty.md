---
hidden: true
---

# Bug Bounty

A bug bounty program for Liquity’s smart contracts is now live. We intend for hackers to look for smart contract vulnerabilities in our system that can lead to loss of funds or locked components.

The preferred way to submit a vulnerability is through Liquity's Vault on [Hats Finance](https://app.hats.finance/bug-bounties/liquity-0xd9a1751269d5506e3528241e3f35d3fbeb974b6b/rewards). If, for any reason, Hats can't be used, vulnerabilities can also be sent using the method described below.

Rewards will be awarded at the sole discretion of Liquity AG. The quality of the report and reproduction instructions can impact the reward. Rewards are denominated and paid out in USD. If both parties agree, rewards can also be paid out in crypto assets.

### Reporting a Vulnerability

Please responsibly disclose any findings to the development team, following these instructions:

* In order to report a vulnerability, please write an email to security@liquity.org with \[SECURITY DISCLOSURE] in the subject of the email.
* For sensitive vulnerabilities, please encrypt the email using this[ PGP key](https://keys.mailvelope.com/pks/lookup?op=get\&search=security@liquity.org) (Fingerprint: D4BA B0E7 3B99 4FC5 79DC 9E0A C640 0C72 C5B8 CA28).
* We will make our best effort to reply in a timely manner and provide a timeline for resolution.
* Please include a detailed report on the vulnerability with clear reproduction steps. The quality of the report can impact the reward amount.

Failure to do so will result in a finding being ineligible for any bounties.

### Scope

In scope for the bug bounty are all the smart contract components of the Liquity V2 protocol. They can be found in the following repository: [https://github.com/liquity/bold](https://github.com/liquity/bold)

Solidity code under the `contracts` directory:&#x20;

`/src`

`├── ActivePool.sol`

`├── AddressesRegistry.sol`

`├── BoldToken.sol`

`├── BorrowerOperations.sol`

`├── CollateralRegistry.sol`

`├── CollSurplusPool.sol`

`├── DefaultPool.sol`

`├── Dependencies`

`│   ├── AddRemoveManagers.sol`

`│   ├── AggregatorV3Interface.sol`

`│   ├── Constants.sol`

`│   ├── IRETHToken.sol`

`│   ├── LiquityBase.sol`

`│   ├── LiquityMath.sol`

`│   └── Ownable.sol`

`├── GasPool.sol`

`├── Interfaces`

`│   ├── IActivePool.sol`

`│   ├── IAddRemoveManagers.sol`

`│   ├── IAddressesRegistry.sol`

`│   ├── IBoldRewardsReceiver.sol`

`│   ├── IBoldToken.sol`

`│   ├── IBorrowerOperations.sol`

`│   ├── ICollateralRegistry.sol`

`│   ├── ICollSurplusPool.sol`

`│   ├── ICommunityIssuance.sol`

`│   ├── ICompositePriceFeed.sol`

`│   ├── IDefaultPool.sol`

`│   ├── IInterestRouter.sol`

`│   ├── ILiquityBase.sol`

`│   ├── ILQTYStaking.sol`

`│   ├── ILQTYToken.sol`

`│   ├── IMultiTroveGetter.sol`

`│   ├── IPriceFeed.sol`

`│   ├── ISortedTroves.sol`

`│   ├── IStabilityPoolEvents.sol`

`│   ├── IStabilityPool.sol`

`│   ├── ITroveEvents.sol`

`│   ├── ITroveManager.sol`

`│   ├── ITroveNFT.sol`

`│   ├── IWETHPriceFeed.sol`

`│   ├── IWETH.sol`

`│   ├── IWSTETHPriceFeed.sol`

`│   └── IWSTETH.sol`

`├── MockInterestRouter.sol`

`├── PriceFeeds`

`│   ├── CompositePriceFeed.sol`

`│   ├── MainnetPriceFeedBase.sol`

`│   ├── RETHPriceFeed.sol`

`│   ├── WETHPriceFeed.sol`

`│   └── WSTETHPriceFeed.sol`

`├── SortedTroves.sol`

`├── StabilityPool.sol`

`├── TroveManager.sol`

`├── TroveNFT.sol`

`├── Types`

`│   ├── BatchId.sol`

`│   ├── LatestBatchData.sol`

`│   ├── LatestTroveData.sol`

`│   ├── TroveChange.sol`

`│   └── TroveId.sol`

`└── Zappers`

&#x20;   `├── GasCompZapper.sol`

&#x20;   `├── Interfaces`

&#x20;   `│   ├── IExchange.sol`

&#x20;   `│   ├── IFlashLoanProvider.sol`

&#x20;   `│   ├── IFlashLoanReceiver.sol`

&#x20;   `│   └── ILeverageZapper.sol`

&#x20;   `├── LeverageLSTZapper.sol`

&#x20;   `├── LeverageWETHZapper.sol`

&#x20;   `├── Modules`

&#x20;   `│   ├── Exchanges`

&#x20;   `│   │   ├── CurveExchange.sol`

&#x20;   `│   │   └── UniV3Exchange.sol`

&#x20;   `│   │   └── HybridCurveUniV3Exchange.sol`

&#x20;   `│   └── FlashLoans`

&#x20;   `│       └── BalancerFlashLoan.sol`

&#x20;   `└── WETHZapper.sol`

### Out of scope

Known issues will not be rewarded:

* [Known issues 1](https://github.com/liquity/bold/issues)
* [Known issues 2](https://github.com/liquity/bold?tab=readme-ov-file#known-issues-and-mitigations)
* [V1 security advisories](https://github.com/liquity/dev/security/advisories)

### Areas of interest

These are some examples of vulnerabilities that would be interesting:

* Stealing tokens or manipulating the token generation process.
* Locking or freezing any of the Liquity V2 contracts.
* Griefing attacks: is it possible to block liquidations, redemptions, borrower operations, rewards distributions, etc.
* Do the desired constraints on borrower operations hold?
* Flash loan exploits
* LQTY token exploits involving the LockupContracts
* Frontend initiated smart contract interactions which unexpectedly impact the user negatively - e.g. MEV risk from withdrawing liquidity from an AMM

### Resources

* [Liquity V2 README](https://github.com/liquity/bold/blob/main/README.md)

### Eligibility

Terms for eligible bounties:

* Only unknown vulnerabilities will be awarded a bounty; in case of duplicate reports, the first report will be awarded the bounty.
* Public disclosure of the vulnerability, before explicit consent from Liquity AG to do so, will make the vulnerability ineligible for a bounty.
* Attempting to exploit the vulnerability in a public Ethereum network will also make it ineligible for a bounty.

\
