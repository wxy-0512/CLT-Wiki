# 資料來源摘要 04：常態母體衍生之隨機函數分配

## 詮釋資料 (Metadata)
- **標題**：Lesson 26: Random Functions Associated with Normal Distributions
- **作者 / 機構**：Penn State University (Eberly College of Science, Department of Statistics)
- **所屬教材 / 課程**：*STAT 414: Introduction to Probability Theory*
- **原始網址**：https://online.stat.psu.edu/stat414/Lesson26
- **匯入狀態**：成功匯入

---

## 主要概念與重點
1. **常態母體下的精確抽樣理論（Exact Sampling Theory）**：
   - 當原始母體本身即為常態分布 $N(\mu, \sigma^2)$ 時，由獨立同分布（i.i.d.）隨機變數 $X_1, X_2, \dots, X_n$ 所構建的線性組合依然是嚴格的常態分布。
   - 樣本平均數 $\bar{X} = \frac{1}{n}\sum_{i=1}^n X_i$ 在任何樣本大小 $n \ge 1$ 之下，皆**精確服從**常態分布，不需依賴樣本數漸近於無限大（非漸近性質）。

2. **動差生成函數（MGF）的理論推導**：
   - 透過動差生成函數性質：
     $$M_{\bar{X}}(t) = \left[ M_X\left(\frac{t}{n}\right) \right]^n$$
   - 代入單一常態變數的 MGF $M_X(t) = \exp\left(\mu t + \frac{\sigma^2 t^2}{2}\right)$，可嚴格證明其產生的動差生成函數完全符合 $N\left(\mu, \frac{\sigma^2}{n}\right)$。

3. **為中央極限定理奠定理論基石**：
   - Lesson 26 確立了「若母體為常態，則平均數必為常態」的基準線。
   - 後續的 Lesson 27（中央極限定理）則將此結論推廣至「即使母體不是常態，只要 $n$ 夠大，平均數也會趨向常態」。

---

## 重要定義與數學公式

- **樣本平均數定義**：
  $$\bar{X} = \frac{1}{n}\sum_{i=1}^n X_i$$

- **常態母體抽樣之精確分布**：
  $$\bar{X} \sim N\left(\mu, \frac{\sigma^2}{n}\right)$$
  - 期望值：$E(\bar{X}) = \mu$
  - 變異數：$Var(\bar{X}) = \frac{\sigma^2}{n}$
  - 標準誤：$SD(\bar{X}) = \frac{\sigma}{\sqrt{n}}$

- **標準化轉化**：
  $$Z = \frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0, 1)$$
