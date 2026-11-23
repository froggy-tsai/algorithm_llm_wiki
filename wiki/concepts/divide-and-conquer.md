# 分治法 (Divide and Conquer)

## 核心想法

分治法是一種演算法設計方式：

1. **Divide（分割）**：將問題實例分成子問題。
2. **Conquer（征服）**：遞迴解決子問題。
3. **Combine（合併）**：合併子問題的解。

子問題數量、子問題大小，以及分割與合併所做的工作共同決定執行時間。常見分析形式為遞迴式 `T(n) = aT(n/b) + f(n)`，可使用[Master theorem](master-theorem.md)分析適用的情形。

## 教材中的演算法

- [Merge sort](../algorithms/sorting/merge-sort.md)：遞迴排序兩個子序列，再線性時間合併。
- [二分搜尋](../algorithms/searching/binary-search.md)：檢查中間元素後，遞迴搜尋一個子陣列。
- [快速冪](../algorithms/numeric/exponentiation.md)：將指數約減半，遞迴計算冪次。
- [分治矩陣乘法](../algorithms/matrix-multiplication/divide-and-conquer.md)與[Strassen 演算法](../algorithms/matrix-multiplication/strassen.md)。
- [VLSI 樹狀配置](../algorithms/layout/vlsi-tree-layout.md)：教材以遞迴關係分析樹嵌入網格的尺寸。

## 來源

- `L3_DivideAndConquer.pdf`，投影片 2–4、54。
