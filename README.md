# iOS 自用装机包

三个自用 App 的未签名 IPA，全部走 **TrollStore** 安装，永久有效不掉签。

**最新：** [v2026.11.08b](https://github.com/wmy2468/ios-apps/releases/tag/v2026.11.08b)

| 文件 | 应用 | 版本 | bundle id | 说明 |
|---|---|---|---|---|
| `ReceiptLedger-v1.2.ipa` | 票记 | 1.2 | `com.wmy2468.receiptledger` | 记账：本地 OCR + 语音 + 多账户 + 转账 + 预算 + 搜索筛选 + 导出 |
| `AIBill-v1.1.ipa` | 智账 AIBill | 1.1 | `com.wmy.aibill` | 记账：通义千问 VL 读图识别（需 API Key、联网） |
| `Qingdan-v1.2.0.ipa` | 清单 Qingdan | 1.2.0 | `com.qingdan.app` | 待办清单 + 到点反复催办，纯本地 |

三个 bundle id 互不相同，**可以同时安装**。

## 安装

1. 手机打开本页 → Releases → 点对应 `.ipa` 下载到「文件」
2. 长按文件 → 共享 → TrollStore
3. TrollStore 里点 Install

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
| v2026.11.08b | 11-08 | **1.2** | 1.1 | 1.2.0 |
| v2026.11.08 | 11-08 | 1.1 | 1.1 | 1.2.0 |

### 票记 1.2 变更

- 新增「转账」类型（账户 → 账户，不计入收支）
- 分类预算：逐类设额度，统计页显示进度，超支标红
- 明细页搜索 + 筛选（月份 / 账户 / 类型）
- 统计页新增「近 6 个月支出」趋势
- 记一笔顶部「常用」：一键复用最近的商户 + 分类 + 账户
