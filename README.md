# iOS 自用装机包

三个自用 App 的未签名 IPA，全部走 **TrollStore** 安装，永久有效不掉签。

| 文件 | 应用 | 版本 | bundle id | 说明 |
|---|---|---|---|---|
| `ReceiptLedger-v1.1.ipa` | 票记 | 1.1 | `com.wmy2468.receiptledger` | 记账：本地 OCR 拍照识别 + 语音 + 多账户 + 预算 + CSV 导出 |
| `AIBill-v1.1.ipa` | 智账 AIBill | 1.1 | `com.wmy.aibill` | 记账：通义千问 VL 读图识别（需 API Key、联网） |
| `Qingdan-v1.2.0.ipa` | 清单 Qingdan | 1.2.0 | `com.qingdan.app` | 待办清单 + 到点反复催办，纯本地 |

三个 bundle id 互不相同，**可以同时安装**。

## 安装

1. 手机打开本页 → Releases → 点对应 `.ipa` 下载到「文件」
2. 长按文件 → 共享 → TrollStore
3. TrollStore 里点 Install

## 源码仓库

- 票记：https://github.com/wmy2468/receipt-ledger
- 智账：https://github.com/wmy2468/aibill-ios
- 清单：https://github.com/wmy2468/qingdan-ipa

## 版本规则

1. **文件名必须带版本号**：`<App>-v<版本>.ipa`，例如 `ReceiptLedger-v1.2.ipa`
2. **每次发版新建 Release**（tag 用日期 `vYYYY.MM.DD`），**不覆盖**已有资产
3. 旧版本永久保留，想回退直接下对应的旧包

## 版本历史

| 日期 | 票记 | 智账 | 清单 |
|---|---|---|---|
| 2026.11.08 | 1.1 | 1.1 | 1.2.0 |

