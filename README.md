<div>
<div align="center">
</div>

# JetAPI中转站

### 多模型 API 接入 · 多线路灵活选择 · 按量计费

面向 AI 开发者的统一 API 接入服务，支持常见开发工具与 SDK 接入。
根据预算和使用场景选择线路，在控制台查看调用用量与费用记录。

**[🌐 访问官网](https://api.jetapi.icu/)** · **[💳 查看价格](https://api.jetapi.icu/pricing)** · **[📚 使用文档](https://api.jetapi.icu/docs)** · **[📡 服务状态](https://api.jetapi.icu/status)**

![Service](https://img.shields.io/badge/Service-API%20Access-2563eb?style=flat-square) ![Clients](https://img.shields.io/badge/Clients-Claude%20Code%20|%20Codex%20CLI-475569?style=flat-square) ![Billing](https://img.shields.io/badge/Billing-Pay%20as%20you%20go-16a34a?style=flat-square)

<div>
</div>

## 📌 导航

- [为什么选择 JetAPI](#-为什么选择-jetapi)
- [快速开始](#-快速开始)
- [线路与参考倍率](#-线路与参考倍率)
- [模型与协议](#-模型与协议)
- [充值和费用说明](#-充值和费用说明)
- [常见问题](#-常见问题)
- [支持与反馈](#-支持与反馈)
- [第三方声明](#-第三方声明)

## ✨ 为什么选择 JetAPI

| 功能 | 说明                                                                           |
| :----- | :------------------------------------------------------------------------------- |
| **多线路选择**     | 在创建 API Key 时选择相应分组，按预算和任务需求切换线路。                      |
| **统一管理**     | 在一个账号中管理密钥、调用额度和用量记录。                                     |
| **开发工具接入**     | 提供 Claude Code、Codex CLI 等客户端的配置入口。                               |
|      |                                                                                |
| **兼容常见协议**     | 支持平台列出的 OpenAI 兼容接口及 Anthropic Messages 接口；具体以所选线路为准。 |
| **按量计费**     | 依据所选模型、线路和实际请求用量扣费，费用可在控制台核对。                     |
| **使用记录**     | 查看请求消耗的 Token 和账单记录，便于排查成本。                                |
| **线路稳定**     | 保证不断连，且倍率低至claude 0.0138、gpt 0.074，                               |

**适用场景**：AI 编程助手、个人开发与测试、SDK 集成、多模型试用和调用成本对比。

## 🚀 快速开始

**1. 创建账号**
打开 [JetAPI 官网](https://api.jetapi.icu/)，按网站提供的登录方式注册或登录。

**2. 选择线路与模型**
查看 [价格页面](https://api.jetapi.icu/pricing)，结合模型能力、接口支持和实际价格选择对应分组。

**3. 创建 API Key**
进入控制台创建密钥。请妥善保管 API Key，**不要将其写入公开仓库、截图或前端代码**。

**4. 配置客户端**
按照 [官方使用文档](https://api.jetapi.icu/docs) 获取对应协议的 Base URL、模型 ID 和客户端配置方法。

**5. 发送测试请求并核对费用**
建议先执行一条小规模测试请求，在控制台确认响应、Token 用量和实际扣费，再开展更大规模调用。

> **提示**：不同线路可能使用不同协议、模型标识及配置方式。请使用文档和控制台提供的真实参数，不要直接将线路显示名称当作官方模型 ID。

## 🧩 模型与协议

以下为此前 README 列示的**平台模型标识示例**，不是对这些名称均属于上游官方公开型号、实时可用或所有线路通用的承诺。

<div>
<details>
<summary><b>Claude 系列（展开查看）</b></summary>
</div>

```text
claude-opus-5-5       claude-opus-5        claude-opus-4-8
claude-sonnet-5-5     claude-sonnet-5      claude-sonnet-4-6
claude-haiku-5-5      claude-fable-5       claude-fable-5-1
claude-fable-5-2
```

相关线路此前列示支持 Anthropic Messages（`/v1/messages`）和 OpenAI 兼容聊天接口（`/v1/chat/completions`）。请以具体线路的文档为准。

<div>
</details>
</div>

<div>
<details>
<summary><b>Codex / GPT 系列（展开查看）</b></summary>
</div>

```text
gpt-6.1-sol      gpt-6.1-terra     gpt-6-astra
gpt-6-sol        gpt-6-luna
gpt-5.6-sol      gpt-5.6-terra     gpt-5.6-luna
gpt-5.5          gpt-5.4-mini
```

<div>
</details>
</div>

<div>
<details>
<summary><b>DeepSeek 系列（展开查看）</b></summary>
</div>

```text
deepseek-v4-pro
deepseek-v4.1-flash
```

<div>
</details>
</div>

<div>
<details>
<summary><b>图像生成（展开查看）</b></summary>
</div>

```text
gpt-image-2.6           gpt-image-2.6-flare       gpt-image-2.6-sunburst
gpt-image-2.5           gpt-image-2.5-flare       gpt-image-2.5-sunburst
```

参考价格为  **$0.012 / 张**

## 💳 充值和费用说明

### 站内额度

此前平台公布的充值换算规则为：

> **充值 ¥1 → 获得界面显示为**  **`$1`** **的站内计费额度。**

### 请求如何计费？

通常需要关注：

1. **模型基准价格**：不同模型的输入、输出 Token 或图片计费基准可能不同。
2. **线路倍率**：不同分组可能采用不同倍率。
3. **缓存计费**：若该模型与线路支持缓存，缓存读取或写入可能采用独立费率；并非所有请求一律按十分之一扣费。
4. **实际记录**：以平台生成的请求账单为最终核对依据。

建议首次使用时先少量充值、发送小请求，并对照价格页面和用量记录确认实际成本。

完整价格及当前政策：[查看 JetAPI 价格](https://api.jetapi.icu/pricing)。

## ❓ 常见问题

<div>
<details>
<summary><b>余额耗尽后会发生什么？</b></summary>
</div>

此前平台规则为：账号额度不足时请求会被拒绝，充值后可继续使用。具体错误码、额度阈值和恢复机制以平台实际规则为准。

<div>
</details>
</div>

<div>
<details>
<summary><b>可以使用 Claude Code 或 Codex CLI 吗？</b></summary>
</div>

平台提供对应的客户端配置入口。请参考 [使用文档](https://api.jetapi.icu/docs) 配置适用的协议、Base URL 和模型 ID；不同版本客户端的配置方法可能有差异。

<div>
</details>
</div>

<div>
<details>
<summary><b>各线路的稳定性是否相同？</b></summary>
</div>

不一定。服务质量受上游状态、限流、模型负载和网络环境等因素影响。可通过 [服务状态页](https://api.jetapi.icu/status) 查看平台发布的监测信息；测试口径和时间窗口应以状态页面说明为准。

<div>
</details>
</div>

<div>
<details>
<summary><b>是否支持退款？</b></summary>
</div>

不允许，建议先小额充值。

<div>
</details>
</div>

<div>
<details>
<summary><b>能否申请发票？</b></summary>
</div>

此前公布的规则为：单笔消费满 ¥100 可联系人工客服申请电子普通发票。是否适用以及申请所需材料，以客服回复及现行政策为准。

<div>
</details>
</div>

<div>
<details>
<summary><b>有邀请奖励吗？</b></summary>
</div>

平台设有邀请返佣机制，参考比例为受邀请用户消费额的 3%。奖励适用范围、结算条件和实际政策以控制台活动规则为准。

<div>
</details>
</div>

## 📮 支持与反馈

- **产品官网**：[api.jetapi.icu](https://api.jetapi.icu/)
- **使用文档**：[查看文档](https://api.jetapi.icu/docs)
- **服务状态**：[查看状态](https://api.jetapi.icu/status)
- **GitHub Issues**：[提交文档问题或使用反馈](https://github.com/Jet-798/JetAPI/issues)
- **交流群**：`255641420`

提交问题时建议提供客户端版本、接口类型、时间范围及**脱敏后的**错误信息。请勿公开 API Key、密码、充值凭证或包含私人内容的完整请求日志。

<div>
<div align="center">
</div>

**让模型接入更灵活，让调用费用更清晰。**

[开始使用](https://api.jetapi.icu/) · [价格与计费](https://api.jetapi.icu/pricing) · [文档](https://api.jetapi.icu/docs)


<div>
</div>
