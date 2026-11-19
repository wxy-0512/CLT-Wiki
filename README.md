# CLT-Wiki：中央極限定理教學 Wiki

> **課程作業專案**  
> **核心主題**：中央極限定理——為什麼平均數會趨近常態分配？

---

## 專案介紹

這個專案是統計學課程的作業，目的是透過「LLM Wiki 建置」的方式，系統性地整理中央極限定理（Central Limit Theorem, CLT）的相關知識，再把知識庫的內容轉化為互動式的 HTML 教學簡報。

整個流程分成幾個步驟：先從開放教科書和大學課程網站讀取資料，整理成結構化的來源摘要（Ingest），再依此撰寫知識文章（Wiki），最後以 Wiki 作為唯一的知識來源，製作一份給初學者看的 HTML 教學簡報，裡面包含數學公式、說明文字，以及一個可以直接操作的抽樣模擬實驗。

---

## Wiki 知識庫

知識庫放在 `wiki/` 資料夾，共有 6 篇文章，以漸進式的學習路徑排列：

| 文章 | 主題 | 主要內容 |
| :--- | :--- | :--- |
| [01-母體與樣本.md](wiki/01-母體與樣本.md) | 母體與樣本 | 為什麼需要抽樣、母體與樣本的定義、母數（$\mu$、$\sigma$）與統計量（$\bar{x}$、$s$）的區別、i.i.d. 假設說明 |
| [02-抽樣分配.md](wiki/02-抽樣分配.md) | 抽樣分配 | 重複抽樣的概念、樣本平均數的分布是什麼、抽樣誤差的來源 |
| [03-樣本平均數.md](wiki/03-樣本平均數.md) | 樣本平均數 | 樣本平均數的期望值與標準誤 $\sigma/\sqrt{n}$、不偏性與線性性質推導、大數法則與 CLT 的嚴格區分 |
| [04-常態分配.md](wiki/04-常態分配.md) | 常態分配 | 標準常態分配的性質、$Z$ 分數的意義、常態分配與 CLT 的關係 |
| [05-中央極限定理.md](wiki/05-中央極限定理.md) | 中央極限定理 | 林德伯格－列維定理的完整陳述、成立條件（有限變異數、$n \ge 30$ 經驗門檻）、柯西分布失效反例 |
| [06-中央極限定理的應用.md](wiki/06-中央極限定理的應用.md) | CLT 的實務應用 | 推論統計的三大支柱、電梯載重安全（總和 CLT）、電商退款稽核（平均數 CLT）、解題決策方法 |

每篇文章都包含：概念介紹、重要定義、數學公式、具體例子、與 CLT 的關聯，以及資料來源標記。

---

## 資料來源

資料存放在 `sources/` 資料夾，共引用 **6 篇**開放教材，全數成功取得：

| 編號 | 教材來源 | 主要貢獻 |
| :---: | :--- | :--- |
| 01 | OpenStax *Introductory Statistics 2e*，第 7.1 節 | 樣本平均數抽樣分配、標準誤公式 |
| 02 | OpenStax *Introductory Business Statistics 2e*，第 7.2 節 | LLN 與 CLT 的分工、商業應用情境 |
| 03 | OpenStax *Introductory Statistics 2e*，第 7.3 節 | 個別值 vs 平均數 vs 總和的題型決策 |
| 04 | Penn State STAT 414，Lesson 26 | 常態母體線性組合、動差生成函數（MGF）推導 |
| 05 | Penn State STAT 414，Lesson 27 | CLT 的嚴格數學陳述、弱收斂性 |
| 06 | OpenStax *Statistics*，第 7 章導言 | 鐘形曲線浮現的直觀解釋、$n \ge 30$ 法則 |

每篇來源都整理成獨立的摘要檔（`source-01.md` ～ `source-06.md`），並彙整在 [`sources/source-index.md`](sources/source-index.md) 中。

**Ingest 流程**：讀取各 URL 的網頁內容 → 擷取標題、機構、核心公式與定義 → 以原創文字整理成摘要 → 建立引用索引 → 作為 Wiki 文章的知識基礎。

---

## HTML 教學簡報

簡報位於 `presentation/index.html`，共 **13 頁**，以初學者為主要閱讀對象。

### 內容架構

| 頁碼 | 主題 |
| :---: | :--- |
| 01 | 封面 |
| 02 | 思考起點：混亂的真實世界（所得分配、骰子、良品率都不是常態） |
| 03 | 直觀機制：正負偏差的對沖效應 |
| 04 | 母體與樣本：局部推論全體 |
| 05 | 抽樣分配：統計量本身的機率分布 |
| 06 | 樣本平均數的期望值與標準誤（$E(\bar{X})=\mu$、$\sigma/\sqrt{n}$） |
| 07 | 兩大機率基石：大數法則（LLN）vs 中央極限定理（CLT）的嚴格對比 |
| 08 | 中央極限定理：定義與數學陳述（Lindeberg-Lévy 定理） |
| 09 | 成立條件與邊界：柯西分布失效反例 |
| 10 | **互動探索實驗室**（詳見下方說明） |
| 11 | 實際應用（一）：電梯載重安全評估 |
| 12 | 實際應用（二）：電商退款稽核 |
| 13 | 課程總結與新手避坑指南 |

### 主要技術特色

- **單一 HTML 檔案**：CSS 與 JavaScript 全數內嵌，不需要安裝任何套件，直接用瀏覽器開啟即可。
- **MathJax 3 數學公式渲染**：支援 `$...$` 行內公式與 `$$...$$` 區塊公式。若無網路連線，頁面頂端會顯示離線提示，公式會以原始語法顯示。
- **投影片導覽**：底部上一頁／下一頁按鈕，同時支援鍵盤左右方向鍵切換。
- **頁尾來源標記**：每頁底部皆標示對應的 Wiki 文章與原始文獻。

### 第 10 頁：互動抽樣模擬實驗室

第 10 頁是整份簡報的核心互動元件，讓使用者自己操作觀察 CLT 的收斂過程：

- **母體模型**：指數分布（$\lambda = 0.2$），理論平均數 $\mu=5.0$、標準差 $\sigma=5.0$，呈嚴重右偏。
- **模擬方式**：每次實驗進行 $R=2500$ 次重複抽樣，每次抽取 $n$ 筆，計算樣本平均數 $\bar{X}$，繪製直方圖。
- **使用者可操作的部分**：
  - 切換樣本容量：$n = 1$、$5$、$30$、$100$
  - 按下「重新抽樣」重新產生一組隨機結果
- **圖表顯示**：
  - 左側 Canvas：母體指數分布曲線（橘黃色）
  - 右側 Canvas：樣本平均數直方圖，$n \ge 5$ 時疊合理論常態曲線（紅線），並以綠色虛線標示 $\mu=5.0$
- **即時統計資訊**：模擬平均數 $\bar{\bar{X}}$、模擬標準誤、理論標準誤 $\sigma/\sqrt{n}$，以及分配形態的文字描述

> **注意**：互動功能的 JavaScript 邏輯已透過統計模擬（PowerShell 腳本）驗證數值正確性。瀏覽器中的視覺效果（Canvas 圖表、按鈕高亮、MathJax 渲染）需要使用者自行開啟 `presentation/index.html` 確認，執行過程中未進行自動化瀏覽器測試。

---

## Workflow 流程

完整的流程規範記錄在 [`workflow/workflow.md`](workflow/workflow.md)，簡要說明如下：

```
資料取得（Node 1）
  → 來源驗證（Node 2）→ sources/*.md
  → 主題拆解與大綱設計（Node 3）
  → Wiki 文章撰寫（Node 4）
  → [Gate 1 內容品質檢核] ──未通過→ 返回 Node 4 修訂
  → 簡報架構設計（Node 6）
  → HTML/CSS/JS 實作（Node 7）
  → [Gate 2 網頁功能測試] ──未通過→ 返回 Node 7 修復
  → 文件整理（Node 9）
  → 交付（Node 10）
```

**兩個品質迴圈**：
- **Loop 1（Wiki 內容迴圈）**：Gate 1 未通過（缺公式、缺例子、公式錯誤）→ 退回修訂 Wiki 文章 → 再次審查。
- **Loop 2（HTML 測試迴圈）**：Gate 2 未通過（公式未渲染、JS 錯誤、版面破裂）→ 退回修復 HTML → 再次測試。

**設計理念**：知識層（Wiki）與呈現層（HTML）的問題分開處理，不讓排版問題影響到知識內容，也不讓知識修訂牽動前端程式碼。

實際執行過程中觸發的修復記錄，詳見 `logs/` 資料夾：

- 數學公式渲染問題（MathJax 3 整合）
- 投影片排版不一致（先嘗試 16:9 鎖定，後改為自適應卡片架構並拆為 13 頁）
- 第 10 頁互動功能除錯（按鈕比對邏輯、MathJax 干擾、直方圖曲線截頂問題）

---

## 如何瀏覽簡報

### 本機開啟

1. 確認有網路連線（MathJax 公式需要從 CDN 載入）
2. 在檔案總管中找到 `presentation/index.html`
3. 用瀏覽器（Chrome、Edge、Firefox 皆可）直接開啟

### GitHub Pages

> **待補充**：本專案尚未發布至 GitHub Pages，部署後請在此填入對應的網址。

---

## 專案資料夾結構

```text
CLT-Wiki/
├── sources/                    # 原始文獻來源與摘要
│   ├── source-01.md            # OpenStax Statistics 2e, 7.1
│   ├── source-02.md            # OpenStax Business Statistics 2e, 7.2
│   ├── source-03.md            # OpenStax Statistics 2e, 7.3
│   ├── source-04.md            # Penn State STAT 414, Lesson 26
│   ├── source-05.md            # Penn State STAT 414, Lesson 27
│   ├── source-06.md            # OpenStax Statistics, Ch.7 Introduction
│   └── source-index.md         # 六篇來源的總覽索引
├── wiki/                       # 知識庫（6 篇主題文章）
│   ├── 01-母體與樣本.md
│   ├── 02-抽樣分配.md
│   ├── 03-樣本平均數.md
│   ├── 04-常態分配.md
│   ├── 05-中央極限定理.md
│   └── 06-中央極限定理的應用.md
├── workflow/                   # 流程規範
│   └── workflow.md             # 完整 Mermaid 流程圖、Node 定義、雙 Loop 說明
├── presentation/               # HTML 教學簡報
│   └── index.html              # 13 頁互動簡報（MathJax 3、Canvas 模擬、鍵盤導覽）
├── logs/                       # 執行紀錄與修復日誌
│   ├── 2026-11-14-ingest-sources-and-wiki.md
│   ├── 2026-11-14-workflow-design.md
│   ├── 2026-11-14-presentation-generation-and-test.md
│   ├── 2026-11-14-mathjax-rendering-fix.md
│   ├── 2026-11-14-slide-layout-and-aspect-ratio-fix.md
│   ├── 2026-11-14-presentation-complete-overhaul.md
│   ├── 2026-11-14-slide-10-interactive-debug-fix.md
│   ├── execution-log.md        # 完整執行紀錄（問題、修復、驗證）
│   └── final-check.md          # 最終檢查清單
└── README.md                   # 本文件
```
