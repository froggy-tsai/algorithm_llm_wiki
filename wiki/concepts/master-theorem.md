# Master theorem

## 適用形式

教材介紹遞迴式：

`T(n) = aT(n/b) + f(n)`

其中 `a` 表示每層子問題數量、`n/b` 表示子問題規模，而 `f(n)` 表示分割與合併等非遞迴工作。比較 `f(n)` 與 `n^(log_b a)`，可依教材列出的三種情況求漸進界：

### Case 1：遞迴子問題的總成長較快

若存在常數 `ε > 0`，且 `f(n) = O(n^(log_b a − ε))`，則：

`T(n) = Θ(n^(log_b a))`

### Case 2：兩者相當（含對數因子）

若 `f(n) = Θ(n^(log_b a) · lg^k n)`，其中常數 `k ≥ 0`，則：

`T(n) = Θ(n^(log_b a) · lg^(k+1) n)`

### Case 3：非遞迴工作較快成長

若存在常數 `ε > 0`，且 `f(n) = Ω(n^(log_b a + ε))`，並符合 regularity condition，則：

`T(n) = Θ(f(n))`

本 Wiki 保留投影片所列條件；若要實際使用 Case 3，須另能確認其 regularity condition 成立。教材投影片未在此處展開該條件的細節。

## 教材例子

- **Merge sort**：`a=2, b=2`，所以 `n^(log_b a)=n`；`f(n)=Θ(n)`，屬於 Case 2 且 `k=0`，故 `T(n)=Θ(n lg n)`。見[Merge sort](../algorithms/sorting/merge-sort.md)。
- **二分搜尋**：`a=1, b=2, f(n)=Θ(1)`，所以 `n^(log_2 1)=1`，屬 Case 2 且 `k=0`，故 `T(n)=Θ(lg n)`。見[二分搜尋](../algorithms/searching/binary-search.md)。
- **一般分治矩陣乘法**：`a=8, b=2, f(n)=Θ(n²)`，遞迴子問題項為 `n³`，屬 Case 1，得到 `Θ(n³)`。見[分治矩陣乘法](../algorithms/matrix-multiplication/divide-and-conquer.md)。
- **Strassen**：`a=7, b=2, f(n)=Θ(n²)`，`n^(log_2 7) ≈ n^2.81`，屬 Case 1，得到 `Θ(n^(lg 7))`。見[Strassen 演算法](../algorithms/matrix-multiplication/strassen.md)。

## 與第一份教材的連結

第一份教材以遞迴樹分析 merge sort，得到 `Θ(n lg n)`；本份教材將 Master theorem 作為另一種分析方式。兩頁都引用各自來源，方便比較推導方法。

## 來源

- `L3_DivideAndConquer.pdf`，投影片 5–6、14–15、32–34、42–45。
- `L1_AnalysisOfAlgorithms-1.pdf`，投影片 38–50（遞迴樹分析）。
