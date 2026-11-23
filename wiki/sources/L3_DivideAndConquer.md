# L3 — Divide and Conquer

## 來源資訊

- 檔案：[`L3_DivideAndConquer.pdf`](../../sources/L3_DivideAndConquer.pdf)
- 課堂標題：*Introduction to Algorithms — Lecture 3: Divide and Conquer*
- 投影片日期：2024-02-19
- PDF 範圍：9 個講義頁面，含投影片 1–54。
- 定位慣例：引用數字為每張投影片左下角印出的投影片編號；講義每頁排約 6 張投影片。

## 內容摘要

1. **分治設計典範及 Master theorem**（投影片 1–6）：定義 divide、conquer、combine 三步驟；重述 Master theorem 三種情況，並用它分析 merge sort。
2. **二分搜尋**（投影片 7–15）：在已排序陣列檢查中間元素，只遞迴搜尋一個子陣列；遞迴式 `T(n)=T(n/2)+Θ(1)`，解為 `Θ(lg n)`。
3. **計算冪次**（投影片 16–18）：比較 naive 的 `Θ(n)` 與將指數減半的 divide-and-conquer 方法 `Θ(lg n)`。
4. **Fibonacci 數列**（投影片 19–26）：比較直接遞迴、由底向上、閉式浮點近似與矩陣遞迴平方；指出直接遞迴為指數時間，底向上 `Θ(n)`，矩陣遞迴平方 `Θ(lg n)`，浮點近似可能捨入失誤。
5. **矩陣乘法**（投影片 27–34）：標準方法為 `Θ(n³)`；直接分治法需要 8 次遞迴乘法，遞迴式為 `T(n)=8T(n/2)+Θ(n²)`，仍為 `Θ(n³)`。
6. **Strassen 演算法**（投影片 35–45）：使用 7 次遞迴乘法和 18 次加減法，`T(n)=7T(n/2)+Θ(n²)=Θ(n^(lg 7))`，指數約 2.81；另列當時約 `n≥32` 的實務觀察及理論最佳指數約 2.376，未附相關演算法細節。
7. **VLSI tree layout 與 H-tree embedding**（投影片 46–53）：分析完整二元樹配置面積 `Θ(n lg n)`，以及 H-tree 嵌入面積 `Θ(n)`。
8. **結論**（投影片 54）：分治是多種演算法設計技巧之一，可用遞迴式和 Master method 分析，並常導向有效率的演算法。

## 投影片主題對照

| 投影片 | 主題 |
|---|---|
| 1–6 | 分治法、merge sort 回顧、Master theorem |
| 7–15 | 二分搜尋及遞迴式 |
| 16–18 | 快速冪 |
| 19–26 | Fibonacci 計算方法 |
| 27–34 | 標準與分治矩陣乘法 |
| 35–45 | Strassen 演算法與分析 |
| 46–53 | VLSI tree layout、H-tree embedding |
| 54 | 結論 |

## 已整理到的 Wiki 頁面

- [分治法](../concepts/divide-and-conquer.md)
- [Master theorem](../concepts/master-theorem.md)
- [二分搜尋](../algorithms/searching/binary-search.md)
- [快速冪](../algorithms/numeric/exponentiation.md)
- [Fibonacci 計算方法](../algorithms/numeric/fibonacci.md)
- [標準矩陣乘法](../algorithms/matrix-multiplication/standard.md)
- [分治矩陣乘法](../algorithms/matrix-multiplication/divide-and-conquer.md)
- [Strassen 演算法](../algorithms/matrix-multiplication/strassen.md)
- [VLSI 樹狀配置](../algorithms/layout/vlsi-tree-layout.md)
- [Merge sort](../algorithms/sorting/merge-sort.md)（整合 L1 和 L3 的分析）
- [遞迴式與遞迴樹](../concepts/recurrences-recursion-tree.md)（連結 Master theorem）

## 待確認／限制

- Fibonacci 定義投影片 19 是動畫過程中的暫時畫面；以投影片 20 完整顯示的 `F₀=0, F₁=1` 作為教材正式定義。
- 本份講義未提供 binary search 對未找到元素或重複元素的介面規格，快速冪完整基底情況也未明示。
- VLSI 與 H-tree 僅記錄投影片提供的模型名稱、遞迴式和漸進結果；沒有補入外部幾何條件。
