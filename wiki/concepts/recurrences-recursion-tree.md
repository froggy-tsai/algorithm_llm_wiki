# 遞迴式與遞迴樹

## 介紹

遞迴演算法可用遞迴式描述輸入縮小後的子問題成本，以及每次呼叫額外執行的工作。遞迴樹把遞迴式展開成樹狀結構，方便逐層加總工作量。

對適用於 `T(n)=aT(n/b)+f(n)` 的分治遞迴式，也可依[Master theorem](master-theorem.md)的條件分析。兩種方法都是教材講授的分析方式，推導細節與適用前提應分別保留。

## Merge sort 的遞迴式

教材給出的形式為：

- `T(n) = Θ(1)`，當 `n = 1`。
- `T(n) = 2T(n/2) + Θ(n)`，當 `n > 1`。

投影片也指出更精確的子問題大小應寫成 `⌈n/2⌉` 與 `⌊n/2⌋`；該差異不影響此處的漸進解。

## 遞迴樹推導

針對 `T(n) = 2T(n/2) + cn`（`c > 0`）：

1. 每個節點的非遞迴工作與該節點子問題大小成正比。
2. 在同一層，子問題大小加總為 `n`，所以每層總工作為 `cn = Θ(n)`。
3. 樹高為 `lg n`（教材圖示的推導）。
4. 葉節點數為 `n`，每個葉節點成本為 `Θ(1)`，所以葉節點總成本為 `Θ(n)`。
5. 將 `Θ(n)` 的每層成本加總約 `lg n` 層，得到 `T(n) = Θ(n lg n)`。

此推導對應 [Merge sort](../algorithms/sorting/merge-sort.md)。L3 另用 Master theorem 得到相同漸進界，見[Master theorem](master-theorem.md)。

## 來源

- `L1_AnalysisOfAlgorithms-1.pdf`，投影片 38–50。
- `L3_DivideAndConquer.pdf`，投影片 3–6（merge sort 與 Master theorem 回顧）。
