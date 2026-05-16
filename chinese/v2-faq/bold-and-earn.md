# BOLD 与收益

### 什么是 BOLD？

BOLD 是 Liquity V2 发行的与美元挂钩的稳定币。它完全去中心化、超额抵押，仅由 WETH、wstETH 和 rETH 支持。

与大多数竞争对手相比，BOLD 在设计上是一种弹性稳定币：&#x20;

* 仅由加密资产支持（无真实世界资产或中心化机构托管）
* 不受抵押品变更和协议升级影响（不可变）
* 可直接赎回（始终能以快速且流动的方式转换）

### 与其他稳定币相比，BOLD 的主要优势是什么？

* BOLD 仅使用最去中心化的资产作为抵押品 - WETH、wstETH 和 rETH&#x20;
* 它始终可以按价值 1 美元赎回为底层资产，这意味着你可以随时将其兑换为支持它的抵押品
* 用于发行 BOLD 的合约是不可变的，不允许任何更改，显著减少了攻击
* BOLD 通过治理引导的协议激励流动性（[PIL](lqty-staking.md#docs-internal-guid-8a7939ae-7fff-d87a-a798-f657d5fd8501)）拥有原生激励，确保始终有足够的流动性来处理交易

### BOLD 的锚定机制是什么？

Liquity V2 通过用户自定义利率实现的市场驱动货币政策，使 BOLD 的锚定能够动态响应代币高于或低于 1 美元的情况。

当 BOLD 交易价格高于 1 美元时，借款人倾向于降低利率，因为[赎回](redemptions-and-delegation.md#what-are-redemptions)风险较低，这使得借入 BOLD 更具吸引力而持有 BOLD 吸引力降低。这有助于将价格向下修正。

相反，当 BOLD 交易价格低于 1 美元时，套利者将发起赎回以恢复锚定。此外，借款人面临的赎回风险促使他们提高利率，增强了对 BOLD（和 Earn 存款）的需求，推动其价格上涨。

<figure><img src="../../english/.gitbook/assets/light - BOLD peg mechanism.png" alt=""><figcaption></figcaption></figure>

### 我如何通过 Liquity v2 赚取收益？

* 稳定池存款（Earn）：通过将 BOLD 存入各个稳定池来赚取协议收入。
* 协议激励流动性（PIL）：为 BOLD 在激励的外部 DEX 上提供流动性。&#x20;
* 质押 LQTY：在质押 LQTY 时从 Liquity V1 获得协议收入，同时积累对流动性激励的投票权。除了引导收入和获得 V1 费用外，LQTY 质押者还可能从第三方获得贿赂（需治理投票）作为额外奖励。

### 存款收益来自哪里？

收益来自两个来源：

* **利息支付：** 每个借贷市场将其 75% 的收入分配给其稳定池存款人（Earners）。使用 BOLD 支付。
* &#x20;**清算收益：** 你的 BOLD 将用于清算抵押不足的贷款，实际上以约 5% 的折扣购买其抵押品。使用（质押的）ETH 支付。

所有收益都是完全可持续、可扩展和"真实"的，没有代币排放和锁定。

### 有锁定期吗？  <a href="#docs-internal-guid-e33469f8-7fff-3873-3b78-742f370cf298" id="docs-internal-guid-e33469f8-7fff-3873-3b78-742f370cf298"></a>

没有锁定期。用户可以随时提取他们的 BOLD 存款。&#x20;

### 存款的预期收益率是多少？ <a href="#docs-internal-guid-9adfe211-7fff-6cdc-ba63-258b45131fbf" id="docs-internal-guid-9adfe211-7fff-6cdc-ba63-258b45131fbf"></a>

收益率代表借款人支付的利率。由于借款人 75% 的利息支付流向 Earn，如果少于 75% 的 BOLD 供应存入相应的稳定池，有效收益率可能超过借贷市场的平均利率。这种收益率放大使 Liquity V2 与竞争对手和货币市场区别开来，在那些市场中，贷款利率不能高于借款利率。

查看历史利率[这里](https://dune.com/liquity/liquity-v2#interest-rates)。

### 为什么有多个稳定池？

目标是：

* 为不同的抵押资产建立独立的借贷市场，拥有各自的市场驱动利率，使用稳定池支持在可用抵押品之间动态分配赎回（链接到"赎回"）。&#x20;
* 通过让存款人控制他们想要在清算时暴露于哪些抵押资产，尽可能地分隔风险，当存入各自的稳定池（Earn）时。

### 稳定池从 V1 到 V2 如何演变？

在 V2 中，稳定池的概念扩展到容纳多个流动性质押代币（LST）和 ETH 作为抵押品，将利息收入和清算收益保留在各自的借贷市场（抵押品）内。因此，每种抵押资产都有自己的稳定池来向 BOLD 存款人分配收益。

此外，V2 中的用户自定义利率影响稳定池存款人（Earn）的收益动态，因为现在收益完全来自用户自定义利率（以 BOLD 计）而不是代币排放，这是完全可持续的。

### 不同稳定池的风险如何不同？

用户可以将其稳定币存入他们选择的稳定池，与他们的风险偏好和他们愿意暴露的抵押品类型保持一致。通过选择与特定 LST 或 ETH 相关的池，参与者可以根据每个 LST 或 ETH 的感知风险和潜在回报来定制他们的风险敞口。

通过为不同抵押品类型提供独立的池，系统允许用户根据每种资产的感知风险和潜在回报来选择他们的敞口。这种分隔有助于管理系统性风险，确保一种资产类别的清算影响不会不成比例地影响整个生态系统。

重要的是要注意，所有 BOLD 持有者（包括存款人）仍然依赖于 BOLD 保持其锚定，对所有 LST 和 ETH 都有敞口。

### 什么是 sBOLD？

sBOLD 是由第三方团队 K3 Capital 构建和维护的自动复利稳定池金库。它旨在为将 BOLD 存入 Liquity V2 稳定池的用户自动化奖励再投资。

* 代币地址：[0x50bd66d59911f5e086ec87ae43c811e0d059dd11](https://etherscan.io/address/0x50bd66d59911f5e086ec87ae43c811e0d059dd11)
* DeDaub 审计：[https://dedaub.com/audits/k3-capital/sbold-may-19-2025/](https://dedaub.com/audits/k3-capital/sbold-may-19-2025/)
* ChainSecurity 审计：[https://www.chainsecurity.com/security-audit/k3-sbold](https://www.chainsecurity.com/security-audit/k3-sbold)
* 代码：[https://github.com/K3Capital/sBOLD](https://github.com/K3Capital/sBOLD)
* Telegram：[sBOLD Offical](https://t.me/sBOLDofficial)

_免责声明：sBOLD 不是由 Liquity 核心团队开发或维护的。在与合约交互之前，请查看审计和代码库。_\
