# 次世代企業級高可用韌性架構演進藍圖 (Remediation Blueprint)

> **Strategic Architecture Hardening & Cloud Infrastructure Assessment Directive**  
> **架構負責人：崇緯 ｜ 審查：元翔**

---

## 專案概述 (Executive Summary)

本專案針對通用基礎娛樂城套版系統架構（M9 / KOOBET 體系）在身分防護、交易連續性、金流容災與即時風控層面所面臨的關鍵挑戰，制定了一套具備金融級標準的**全域高可用韌性架構演進藍圖**。

系統從「外牆邊緣防護」延伸至「屋內核心業務邏輯」，全面規劃了 **18 項關鍵工程任務**、**四大核心採購與技術護城河組件**，以及完整的**每月維運成本（Monthly OPEX）雙幣精算模型**。

---

## 核心演進四大支柱 (The 4 Pillars)

1. **全域零信任身分安全 (IAM & Bastion)**
   * 超管入口全面強制綁定 WebAuthn / FIDO2 硬體鎖 (YubiKey 5) 與 TOTP (Google 2FA)。
   * 財務大額出金實施「雙人覆核機制 (Four-Eyes Principle)」與不可竄改集中日誌 (WORM Audit Log)。
2. **金融級高彈性清算交換矩陣 (Resilient Payment Switch)**
   * 建立多商戶健康探針心跳機制，通道異常 2 秒內無感自動熔斷切換。
   * 動態隨機微額小數點尾數對帳池，實現 100% 免人工秒級精準銷單。
3. **分散式事務強一致性機制 (High-Concurrency SAGA Consistency)**
   * 錢包下注與派彩全面重構為 SAGA 分散式事務補償架構，杜絕廠商 API 逾時引起的卡額與漏單。
   * `transaction_id` 全域 Redlock 鎖定與資料庫唯一索引，保證 5,000+ TPS 下帳務 100% ACID 一致性。
4. **流式大數據即時風控決策 (Real-Time Streaming Risk Engine)**
   * 部署 Apache Flink 實時流計算，500ms 內毫秒級阻斷真人百家樂莊閒對沖與體育雙邊打水。
   * 整合高級商業設備指紋（Fingerprint Pro），阻擋群控模擬器多開刷首存。

---

## 每月固定維運費用精算 (Monthly OPEX Budget)

> 基準即時匯率換算：**1 USD = 31.70 TWD**

| 預算類別 | 採購服務與核心組件 | 穩健成長版 (Growth Tier) | 旗艦雙活版 (Enterprise Tier) |
| :--- | :--- | :---: | :---: |
| **外牆邊緣防禦** | Cloudflare Enterprise + Bot Management | $3,500 USD (NT$ 110,950) | $6,000 USD (NT$ 190,200) |
| **屋內身分治理** | Okta IAM + Teleport 堡壘機 + YubiKey 5 折舊 | $950 USD (NT$ 30,115) | $1,800 USD (NT$ 57,060) |
| **金流通道容災** | 4~5 家備用商戶底費 + 泰國本地 OTP 網關 | $1,450 USD (NT$ 45,965) | $2,700 USD (NT$ 85,590) |
| **智能風控授權** | Fingerprint Pro 設備指紋 + IPQS 威脅黑名單 API | $1,200 USD (NT$ 38,040) | $2,600 USD (NT$ 82,420) |
| **雲端基礎設施** | AWS EKS + Aurora MySQL + MSK Kafka + Redis + 頻寬 | $3,800 USD (NT$ 120,460) | $11,000 USD (NT$ 348,700) |
| **合計每月固定支出** | **全棧企業級高可用防禦閉環** | **$10,000 USD / 月<br>(約 NT$ 317,000)** | **$21,800 USD / 月<br>(約 NT$ 690,960)** |

---

## 互動式儀表板檔案說明

* `index.html` / `remediation_roadmap.html`：
  次世代企業級高可用韌性架構演進藍圖互動網頁（包含 18 項任務打勾進度環、動態成熟度雷達圖、雙模代理分潤計算器、採購矩陣與每月維運雙幣精算表）。
* `casino_architecture_audit.html`：
  白標套版 vs 國際旗艦平台架構對比與診斷儀表板。

---

## 署名與簽核

* **架構負責人**：崇緯
* **審查簽核**：元翔
