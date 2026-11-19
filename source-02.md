# 資料來源摘要 02：中央極限定理的應用與大數法則

## 詮釋資料 (Metadata)
- **標題**：7.2 Using the Central Limit Theorem
- **作者 / 機構**：OpenStax (Alexander Holmes, Barbara Illowsky, Susan Dean 等)
- **所屬教材**：*Introductory Business Statistics 2e*
- **原始網址**：https://openstax.org/books/introductory-business-statistics-2e/pages/7-2-using-the-central-limit-theorem
- **匯入狀態**：成功匯入

---

## 主要概念與重點
1. **大數法則（Law of Large Numbers, LLN）與中央極限定理（CLT）之分工**：
   - **大數法則**證明了「中心點在哪裡」：隨著樣本數 $n$ 不斷增大，樣本平均數 $\bar{x}$ 在機率上會無限逼近真實母體平均數 $\mu$。
   - **中央極限定理**說明了「分布形狀長怎樣」：指出當 $n$ 夠大時，樣本平均數圍繞 $\mu$ 散佈的形態會呈現鐘形的常態曲線。

2. **商業決策與推論統計中的核心推論**：
   - 商業情境中的許多原始數據（如顧客消費金額、電話通話時間、等候時間）往往具有極端偏態或非對稱性。
   - CLT 使得決策者不必依賴母體的未知分布，只要抽樣規模合理（$n \ge 30$），就能以常態機率模型評估平均水準的風險與期望值。

3. **標準誤（Standard Error）的實務意涵**：
   - 標準誤 $\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$ 衡量了抽樣誤差的幅度。
   - 增加樣本容量可以降低估計的不確定性，為建立信賴區間與商業決策門檻提供數理依據。

---

## 重要定義與數學公式

- **大數法則期望關係**：
  $$E(\bar{X}) = \mu$$

- **樣本平均數的標準誤**：
  $$\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$$

- **機率計算之 $Z$ 分數轉化**：
  $$Z = \frac{\bar{x} - \mu}{\frac{\sigma}{\sqrt{n}}}$$
  透過查標準常態分布表或累積分布函數（CDF），可計算樣本平均值落於特定區間的機率。
