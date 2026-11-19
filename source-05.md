# 資料來源摘要 05：中央極限定理的嚴格機率論述

## 詮釋資料 (Metadata)
- **標題**：Lesson 27: The Central Limit Theorem
- **作者 / 機構**：Penn State University (Eberly College of Science, Department of Statistics)
- **所屬教材 / 課程**：*STAT 414: Introduction to Probability Theory*
- **原始網址**：https://online.stat.psu.edu/stat414/Lesson27
- **匯入狀態**：成功匯入

---

## 主要概念與重點
1. **林德伯格－列維中央極限定理（Lindeberg-Lévy CLT）之定義**：
   - 設 $X_1, X_2, \dots, X_n$ 為來自任意母體的獨立同分布（i.i.d.）隨機變數序列，只要其具備有限期望值 $\mu$ 與有限變異數 $\sigma^2 < \infty$。
   - 隨著樣本數 $n \to \infty$，標準化樣本平均數在**分布上收斂（Convergence in Distribution, $\xrightarrow{d}$）**至標準常態分布 $N(0, 1)$。

2. **理論證明視角（動差生成函數極限）**：
   - 利用泰勒展開式展開變數的動差生成函數，當 $n \to \infty$ 時，標準化和的 MGF 極限為：
     $$\lim_{n \to \infty} M_{Z_n}(t) = e^{\frac{t^2}{2}}$$
   - 此即標準常態分布的動差生成函數，由此確立了弱極限定理在數學上的嚴密性。

3. **兩種等價表述方式**：
   - **平均數型式**：$\bar{X}$ 的漸近分布為 $N\left(\mu, \frac{\sigma^2}{n}\right)$。
   - **總和型式**：$Y = \sum_{i=1}^n X_i$ 的漸近分布為 $N\left(n\mu, n\sigma^2\right)$。

4. **後續延伸與離散逼近**：
   - Lesson 27 亦指出 CLT 為離散隨機變數（如二項分布、卜瓦松分布）以常態曲線進行連續性修正逼近提供了理論依據。

---

## 重要定義與數學公式

- **中央極限定理數學陳述**：
  $$Z_n = \frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}} = \frac{\sum_{i=1}^n X_i - n\mu}{\sigma \sqrt{n}} \xrightarrow{d} N(0, 1) \quad (\text{as } n \to \infty)$$

- **累積分布函數收斂性**：
  $$\lim_{n \to \infty} P\left( \frac{\bar{X} - \mu}{\sigma/\sqrt{n}} \le z \right) = \Phi(z) = \int_{-\infty}^z \frac{1}{\sqrt{2\pi}} e^{-\frac{u^2}{2}} \, du$$
