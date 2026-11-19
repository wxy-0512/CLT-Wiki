# 資料來源摘要 01：樣本平均數的中央極限定理

## 詮釋資料 (Metadata)
- **標題**：7.1 The Central Limit Theorem for Sample Means (Averages)
- **作者 / 機構**：OpenStax (Barbara Illowsky, Susan Dean 等)
- **所屬教材**：*Introductory Statistics 2e*
- **原始網址**：https://openstax.org/books/introductory-statistics-2e/pages/7-1-the-central-limit-theorem-for-sample-means-averages
- **匯入狀態**：成功匯入

---

## 主要概念與重點
1. **抽樣分配的核心現象**：
   - 當從任何母體（無論其原始機率分布是已知或未知、對稱或偏態）中重複抽取容量為 $n$ 的隨機樣本時，隨著樣本數 $n$ 的增加，**樣本平均數（$\bar{X}$）的機率分布將趨近於常態分布**。
   - 這一由所有可能樣本平均數組成的機率分布，稱為「樣本平均數的抽樣分配（Sampling Distribution of the Mean）」。

2. **抽樣分配的母數特徵**：
   - **樣本平均數的期望值（中心）**：恰好等於母體平均數 $\mu$。即 $\mu_{\bar{x}} = \mu$。
   - **樣本平均數的標準差（標準誤）**：等於母體標準差 $\sigma$ 除以樣本數 $n$ 的平方根。即 $\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$。
   - 當 $n$ 增加時，標準誤會逐漸縮小，表示樣本平均數會越來越緊密地集中在母體平均數周圍。

3. **樣本數門檻之經驗法則**：
   - 在實務應用中，通常以 $n \ge 30$ 作為中央極限定理發揮作用的一般門檻。
   - 若母體本身已經是常態分布，則不論樣本數 $n$ 大小為何，樣本平均數的分布皆為常態分布。

---

## 重要定義與數學公式

- **樣本平均數的常態表示法**：
  $$\bar{X} \sim N\left(\mu, \frac{\sigma}{\sqrt{n}}\right)$$

- **樣本平均數的標準化 $Z$ 分數**：
  $$Z = \frac{\bar{x} - \mu_{\bar{x}}}{\sigma_{\bar{x}}} = \frac{\bar{x} - \mu}{\frac{\sigma}{\sqrt{n}}}$$
  其中：
  - $\bar{x}$：觀察到的樣本平均數
  - $\mu$：母體平均數
  - $\sigma$：母體標準差
  - $n$：每個樣本包含的觀測值數量（樣本容量）
