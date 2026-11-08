# iOS 自用装机包

三个自用 App 的未签名 IPA，全部走 **TrollStore** 安装，永久有效不掉签。

**最新：** [v2026.11.08c](https://github.com/wmy2468/ios-apps/releases/tag/v2026.11.08c)

| 文件 | 应用 | 版本 | bundle id | 说明 |
|---|---|---|---|---|
| `ReceiptLedger-v1.3.ipa` | 票记 | 1.3 | `com.wmy2468.receiptledger` | 记账：OCR（小票/微信/支付宝截图）+ 语音 + 多账户 + 转账 + 预算 + 账单导入 + 资产负债 + 导出 |
| `AIBill-v1.1.ipa` | 智账 AIBill | 1.1 | `com.wmy.aibill` | 记账：通义千问 VL 读图识别（需 API Key、联网） |
| `Qingdan-v1.2.0.ipa` | 清单 Qingdan | 1.2.0 | `com.qingdan.app` | 待办清单 + 到点反复催办，纯本地 |

三个 bundle id 互不相同，**可以同时安装**。

## 安装

1. 手机打开本页 → Releases → 点对应 `.ipa` 下载到「文件」
2. 长按文件 → 共享 → TrollStore
3. TrollStore 里点 Install

**Release 下载报 504 时（GitHub 网关抽风）**，用 raw 备用直链：

```
https://raw.githubusercontent.com/wmy2468/ios-apps/main/files/ReceiptLedger-v1.3.ipa
```

`files/` 目录只放最新的票记包，Release 里的历史版本不动。

覆盖升级：同 bundle id 装新版本会替换旧 App，数据一般保留；升级前建议先在设置里导一份 CSV。

## 源码仓库

- 票记：https://github.com/wmy2468/receipt-ledger
- 智账：https://github.com/wmy2468/aibill-ios
- 清单：https://github.com/wmy2468/qingdan-ipa

## 版本规则

1. **文件名必须带版本号**：`<App>-v<版本>.ipa`，例如 `ReceiptLedger-v1.2.ipa`
2. **每次发版新建 Release**（tag 用日期 `vYYYY.MM.DD`，同日多次发版加字母后缀），**不覆盖**已有资产
3. 旧版本永久保留，想回退直接下对应的旧包

## 版本历史

| Release | 日期 | 票记 | 智账 | 清单 |
|---|---|---|---|---|
| v2026.11.08c | 11-08 | **1.3** | 1.1 | 1.2.0 |
| v2026.11.08b | 11-08 | 1.2 | 1.1 | 1.2.0 |
| v2026.11.08 | 11-08 | 1.1 | 1.1 | 1.2.0 |

### 票记 1.3 变更

- 微信 / 支付宝**截图识别**优化：自动识别账户（微信 / 支付宝）、金额取两位小数、商户从「收款方 / 转账给」等字段提取
- **账单导入**：微信「账单明细.csv」、支付宝「交易明细.csv」，自动识别 UTF-8 / GB18030 编码，按交易单号去重
- **资产负债**：账户可设初始余额与信用卡标记，统计页显示 资产 / 负债 / 净资产

### 票记 1.2 变更

- 新增「转账」类型（账户 → 账户，不计入收支）
- 分类预算：逐类设额度，统计页显示进度，超支标红
- 明细页搜索 + 筛选（月份 / 账户 / 类型）
- 统计页新增「近 6 个月支出」趋势
- 记一笔顶部「常用」：一键复用最近的商户 + 分类 + 账户
