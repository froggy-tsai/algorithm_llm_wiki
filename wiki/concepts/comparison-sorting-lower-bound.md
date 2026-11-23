# 比較排序的決策樹下界

## 決策樹模型

決策樹可表示 comparison sort 在固定輸入規模 `n` 下所有可能比較路徑：

- 每個內部節點標記一次元素比較 `i:j`。
- 左右子樹分別代表比較結果 `aᵢ ≤ aⱼ` 或 `aᵢ > aⱼ`。
- 每個葉節點代表一種已確定的元素排列結果。
- 演算法在該輸入上的執行時間對應走過的路徑長度；最壞情況時間對應決策樹高度。

## 下界推導

任何能排序 `n` 個互異元素的決策樹至少需要 `n!` 個葉節點，因為輸入可能有 `n!` 種排列。高度為 `h` 的二元樹至多有 `2^h` 個葉節點，因此：

`2^h ≥ n!`

取對數並使用 Stirling 公式的下界 `n! ≥ (n/e)^n`：

`h ≥ lg(n!) ≥ lg((n/e)^n) = n lg n − n lg e = Ω(n lg n)`

所以任何 comparison sort 的最壞情況比較次數至少為 `Ω(n lg n)`。

## 推論與適用範圍

- [Heapsort](../algorithms/sorting/heapsort.md) 與 [merge sort](../algorithms/sorting/merge-sort.md) 的最壞情況比較排序時間為 `O(n lg n)`，達到此比較排序下界的漸進階，因此教材稱兩者 asymptotically optimal。
- 此下界限於依元素兩兩比較來決定順序的 comparison sorts。
- Counting sort 不比較元素；radix sort 可用穩定的 counting sort 作為每一趟排序，因此它們不違反此下界。其線性時間依賴鍵值範圍、位數及基數等條件，詳見[counting sort](../algorithms/sorting/counting-sort.md)和[radix sort](../algorithms/sorting/radix-sort.md)。

## 來源

- `L5_SortingLowerBounds.pdf`，投影片 2–10、28–29。

