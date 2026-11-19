# 資料來源摘要 03：中央極限定理的使用與題型判斷

## 詮釋資料 (Metadata)
- **標題**：7.3 Using the Central Limit Theorem
- **作者 / 機構**：OpenStax (Barbara Illowsky, Susan Dean 等)
- **所屬教材**：*Introductory Statistics 2e*
- **原始網址**：https://openstax.org/books/introductory-statistics-2e/pages/7-3-using-the-central-limit-theorem
- **匯入狀態**：成功匯入

---

## 主要概念與重點
1. **解題與應用情境的分類決策準則**：
   - **單一數值機率問題（Individual Value $X$）**：**不可**使用 CLT。必須依賴原始母體本身的機率分布（如題目必須明示母體為常態分布，方能計算標準分數）。
   - **樣本平均數機率問題（Sample Mean $\bar{X}$）**：使用**樣本平均數的 CLT**，其抽樣分布為 $\bar{X} \sim N\left(\mu, \frac{\sigma}{\sqrt{n}}\right)$。
   - **樣本總和機率問題（Sum / Total $\Sigma X$）**：使用**樣本總和的 CLT**，其抽樣分布為 $\Sigma X \sim N(n\mu, \sqrt{n}\sigma)$。

2. **百分位數（Percentile）逆向計算**：
   - 不僅可用於計算「機率值」，亦可用於由給定機率求出臨界值。
   - 例如求樣本平均數的第 90 百分位數，先求出累積機率為 0.90 所對應的標準常態 $Z$ 分數，再藉由 $\bar{x} = \mu + Z \cdot \left(\frac{\sigma}{\sqrt{n}}\right)$ 反推。

3. **樣本容量在總和分配與平均數分配中的角色**：
   - 當樣本總和累加時，期望值變大為 $n\mu$，標準差放大為 $\sqrt{n}\sigma$。
   - 當取平均時，期望值保持 $\mu$，標準差縮小為 $\frac{\sigma}{\sqrt{n}}$。兩者互為鏡像，本質皆遵循常態逼近。

---

## 重要定義與數學公式

- **樣本平均數的分布與轉換**：
  $$\bar{X} \sim N\left(\mu, \frac{\sigma}{\sqrt{n}}\right), \quad Z = \frac{\bar{x} - \mu}{\frac{\sigma}{\sqrt{n}}}$$

- **樣本總和的分布與轉換**：
  $$\Sigma X \sim N\left(n\mu, \sqrt{n}\sigma\right), \quad Z = \frac{\Sigma x - n\mu}{\sqrt{n}\sigma}$$

- **百分位數逆推公式**：
  $$\bar{x} = \mu + Z \left(\frac{\sigma}{\sqrt{n}}\right)$$
  $$\Sigma x = n\mu + Z (\sqrt{n}\sigma)$$
