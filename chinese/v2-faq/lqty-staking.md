# LQTY 质押与投票

### 质押 LQTY 有什么好处？ <a href="#docs-internal-guid-cc9af61b-7fff-453e-92d8-d2cb106c7d5d" id="docs-internal-guid-cc9af61b-7fff-453e-92d8-d2cb106c7d5d"></a>

在 Liquity V2 中质押你的 LQTY 可以解锁独特的双重奖励机会。你不仅获得了对 Liquity V2 未来的影响力，而且你的质押还继续从 Liquity V1 赚取 LUSD 和 ETH 奖励。这种强大的协同作用确保你同时利用 V1 的稳定性和 V2 的创新。

除了投票权，投票者还可能从外部项目获得付款（"贿赂"）。

查看关于[如何质押](https://x.com/LiquityProtocol/status/1936885520203956391)的指南。

### 有锁定期吗？ <a href="#docs-internal-guid-4dbf0bb4-7fff-5281-01ca-d74c5c49d1c1" id="docs-internal-guid-4dbf0bb4-7fff-5281-01ca-d74c5c49d1c1"></a>

没有，没有锁定期。你可以随时提取 LQTY。

但请注意，当你提取时，你会失去累积的"额外"投票权。

### 什么是协议激励流动性（PIL）？ <a href="#docs-internal-guid-8a7939ae-7fff-d87a-a798-f657d5fd8501" id="docs-internal-guid-8a7939ae-7fff-d87a-a798-f657d5fd8501"></a>

这是 Liquity v2 中一种新颖的可持续和自适应激励机制。它将协议 25% 的收入引导到外部项目，旨在改善 BOLD 流动性并刺激整个 Liquity 生态系统的增长。

在此[文章](https://www.liquity.org/blog/directing-protocol-incentivized-liquidity-with-lqty)中阅读更多关于 PIL 和投票的信息。

### 激励来自哪里？ <a href="#docs-internal-guid-266699b3-7fff-4534-ba95-bd541a00496d" id="docs-internal-guid-266699b3-7fff-4534-ba95-bd541a00496d"></a>

每个 Trove 每秒都在以 BOLD 产生利息。这些收益的全部持续分为两个流：稳定池收入和协议流动性激励。百分比硬编码为 75% 和 25%，因此只要系统中有活跃的借款人，PIL 机制就会有预算。

示例：如果 BOLD 的市值为 2 亿，平均利率为 10%，那么 PIL 每年可支配 500 万 BOLD。

### 我如何对项目进行投票？ <a href="#docs-internal-guid-02737f00-7fff-ee7a-06f6-83e67101000f" id="docs-internal-guid-02737f00-7fff-ee7a-06f6-83e67101000f"></a>

要投票，你需要在[前端](https://www.liquity.org/frontend-v2)上质押你的 LQTY。

一旦质押，用户在总协议投票权中的份额由时间加权计算确定。

拥有投票权的用户可以根据自己的意愿权衡项目，按自己的喜好分配投票。这些用户可以从任何项目组合中进行选择，他们的选择在未来的投票期间保持设置，直到他们更改它。

投票在每周周期内进行，该周期从以太坊上每周四 00:00 UTC 之后的区块开始，到下周三 23:59:59 UTC 的最后一个区块结束。

投票过程分为两类：赞成票和反对票（否决）。在每个周期内，可以对项目进行赞成票和反对票，但在周期结束前的最后 24 小时内只能进行反对票。在每个周期的最后 24 小时内，现有投票仍然可以被移除并重新分配以反对项目。

有关项目的提案和讨论，请访问[投票论坛](https://voting.liquity.org/)。

可以在此 Dune [仪表板](https://dune.com/liquity/protocol-incentivized-liquidity)中查看过去的投票轮次。

### 我需要每周投票吗？ <a href="#docs-internal-guid-c36c3153-7fff-1abc-8f12-2131b7c72d57" id="docs-internal-guid-c36c3153-7fff-1abc-8f12-2131b7c72d57"></a>

不需要，上一轮的投票会延续到下一轮。\
\
建议关注新项目以及你已经投票的项目。了解新项目可以让你了解可能更好地分配投票的机会。此外，以前投票的项目可能会被修改或升级，如果发生变化，你最初投票的原因可能不再有效。

### 我如何累积投票权？ <a href="#docs-internal-guid-c36c3153-7fff-1abc-8f12-2131b7c72d57" id="docs-internal-guid-c36c3153-7fff-1abc-8f12-2131b7c72d57"></a>

用户的投票权与质押的 LQTY 成正比，但随时间线性增长。&#x20;

`投票权 = LQTY 质押量 × 质押年龄`

<figure><img src="../../english/.gitbook/assets/voting1.png" alt=""><figcaption></figcaption></figure>

上图显示了四个用户 A、B、C 和 D 在不同时间质押相同金额的个人投票权。通过将他们的个人投票权除以总投票权，我们可以确定相对投票权分布：

<figure><img src="../../english/.gitbook/assets/voting2.png" alt=""><figcaption></figcaption></figure>

用户质押时间越长，取消质押时失去的投票权就越多。

### 我以后可以增加质押或部分减少质押吗？ <a href="#docs-internal-guid-dfddb7da-7fff-d157-26a8-92ef7c49015f" id="docs-internal-guid-dfddb7da-7fff-d157-26a8-92ef7c49015f"></a>

是的，可以增加或减少现有质押。请记住，新增加的金额从投票权 0 开始，而减少质押将使你的质押年龄保持不变。

添加到现有质押的新金额从投票权 0 开始（以防止类似闪电贷的滥用）：因此，在质押后，总投票权保持不变（线是连续的），但斜率增加。相反，在取消质押时，用户的投票权会立即下降（不连续），除了斜率明显减少。

### 如何提出新项目？ <a href="#docs-internal-guid-3bc52c98-7fff-48a0-f2fa-6bc1e30a444d" id="docs-internal-guid-3bc52c98-7fff-48a0-f2fa-6bc1e30a444d"></a>

任何拥有所有质押 LQTY 总投票权至少 0.01% 并支付 100 BOLD 注册费的用户都可以提出新激励。

从技术上讲，任何以太坊地址都可以接收协议流动性激励，但通常建议为项目创建智能合约，其中包含引导任何接收资金所需的任何逻辑，这些资金将以 BOLD 支付。此合约应由提议者适当审查和审计，以确保其安全并按预期工作。

一旦项目部署，就可以注册。

&#x20;首先，在[这里](https://etherscan.io/address/0x6440f144b7e50D6a8439336510312d2F54beB01D#writeContract)调用 `approve` 函数：

-   输入 `spender` 地址：`0x807DEf5E7d057DF05C796F4bc75C3Fe82Bd6EeE1`
-   在 `amount` 下输入至少 100 BOLD（100 \* 1e18）

然后在[这里](https://etherscan.io/address/0x807def5e7d057df05c796f4bc75c3fe82bd6eee1#writeContract)注册，在 `registerInitiative` 下输入你的 `_initiative` 地址

一旦注册，项目可以在下一个周期被投票。出于效率原因，只有将获得至少 2% 投票的项目才有资格。在四个或更多连续周期内未能达到此阈值的项目可以被无需许可地取消注册。

### 激励如何分配？ <a href="#docs-internal-guid-fa52da7b-7fff-8c78-7cd7-40b59a14a1da" id="docs-internal-guid-fa52da7b-7fff-8c78-7cd7-40b59a14a1da"></a>

协议流动性激励会累积，然后每周分配给所有符合条件的项目或目标地址。&#x20;

要获得激励资格，项目必须达到所有投票的 2% 的相对阈值。

激励分配是所有符合条件项目之间权重加权的函数：激励按相对投票比例分配（只要项目符合条件，不计算反对票）。

激励**必须在同一周认领**，否则它们将重新分配到下周的轮次。

### 被反对的项目会怎样？

拥有超过 2% 相对阈值的赞成票，并且收到的反对票多于赞成票的项目，如果反对票数量超过赞成票数量，将被取消激励资格。这类项目可以被任何人取消注册。

### 不活跃或不受欢迎的项目会怎样？

连续 4 个周期（周）未能达到资格阈值或最低每周认领的项目可以被任何人取消注册。

### 我的钱包中收到新合约警告

Liquity V2 使用代理模式进行质押，当有人首次质押 LQTY 时创建一个新的"UserProxy"合约。因此，某些钱包可能会将此标记为"新合约警告"。
