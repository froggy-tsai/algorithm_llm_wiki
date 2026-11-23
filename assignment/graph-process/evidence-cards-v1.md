# Evidence Cards v1 — 排序演算法教學簡報

## 狀態與範圍檢查

- 狀態：候選範圍，待人工確認大綱。
- 作業目標：用 Wiki 作為知識來源，製作讓初學者理解基本概念的教學 HTML 簡報。
- 使用者目標：快速、有效地複習演算法。
- 候選簡報範圍：排序演算法，從比較排序到線性時間排序。
- Wiki 覆蓋檢查：此範圍有排序問題、比較排序下界，以及六種排序演算法的來源支持，足以形成一份連貫的基本教學。Wiki 內的二分搜尋、矩陣乘法、Fibonacci、VLSI 等內容與本次排序教學主線無直接必要關係，先不納入。
- 資料限制：只使用 `wiki/` 中可回溯至使用者提供 PPT 的內容；不以外部搜尋補充。

## 證據卡

| ID | 可用於簡報的教材主張 | 必須保留的條件／界線 | Wiki 頁面 | 原始教材定位 |
|---|---|---|---|---|
| EC-01 | 排序輸入是數列，輸出是包含相同元素且依非遞減順序排列的數列。 | 以教材定義和示例說明排序目標。 | [插入排序](../../wiki/algorithms/sorting/insertion-sort.md) | L1 投影片 4 |
| EC-02 | Comparison sort 以元素間比較決定相對順序；決策樹模型導出最壞情況下界 `Ω(n lg n)`。 | 下界限於 comparison sorts；推導以互異元素的 `n!` 種排列為基礎。不得用來否定 counting／radix sort。 | [決策樹下界](../../wiki/concepts/comparison-sorting-lower-bound.md) | L5 投影片 2–10 |
| EC-03 | 插入排序逐一將下一個元素插入已排序前綴；教材列出的最壞及平均時間為 `Θ(n²)`。 | 平均分析假設所有排列等可能；教材沒有提供明確的最好情況 Θ 式。 | [插入排序](../../wiki/algorithms/sorting/insertion-sort.md) | L1 投影片 5–23 |
| EC-04 | Merge sort 遞迴排序兩半，再以線性時間合併，時間為 `Θ(n lg n)`。 | 不把教材的遞迴分析延伸成未提及的空間複雜度。 | [Merge sort](../../wiki/algorithms/sorting/merge-sort.md) | L1 投影片 24–50；L3 投影片 3–6 |
| EC-05 | Heapsort 先建 max-heap，再反覆把最大元素移到陣列尾端；建堆為 `O(n)`，整體排序為 `O(n lg n)`。 | 保留教材的 `O` 上界記號；heap 的示例索引從 1 開始。 | [Heapsort](../../wiki/algorithms/sorting/heapsort.md) | L4a 投影片 2–26 |
| EC-06 | Quicksort 使用 pivot partition，再遞迴排序兩側；固定首元素 pivot 的最壞情況為 `Θ(n²)`。 | 隨機化期望上界 `O(n lg n)` 的推導假設輸入元素互異、隨機選擇獨立；不能說每次執行都保證此時間。 | [Quicksort](../../wiki/algorithms/sorting/quicksort.md) | L4 投影片 2–47 |
| EC-07 | Counting sort 針對鍵值在 `1..k` 的輸入，時間 `Θ(n+k)`，且為穩定排序；當 `k=O(n)` 時為線性時間。 | 線性時間依賴鍵值範圍相對 `n` 不大；它不比較輸入元素。 | [Counting sort](../../wiki/algorithms/sorting/counting-sort.md) | L5 投影片 11–30 |
| EC-08 | Radix sort 從最低位開始逐趟排序；每趟使用穩定排序，總時間依位數 `b` 和每趟位元數 `r` 而定。 | 教材公式為 `Θ((b/r)(n+2^r))`；近線性結論須符合教材的數值範圍、基數和位數條件。 | [Radix sort](../../wiki/algorithms/sorting/radix-sort.md) | L5 投影片 31–39 |
| EC-09 | Heapsort 與 merge sort 達到 comparison-sort 的 `Ω(n lg n)` 最壞情況下界階；counting／radix sort 不屬於比較排序模型。 | 不把漸進結論說成所有輸入、硬體或實作下的速度排名。 | [決策樹下界](../../wiki/concepts/comparison-sorting-lower-bound.md) | L5 投影片 9–10、28–29 |

## 待人工確認事項

1. 是否接受以「排序演算法：從比較排序到線性時間排序」作為本次 HTML 簡報範圍？
2. 是否接受在同一份簡報中介紹以上六種排序演算法？
3. 若要縮小，優先保留哪些演算法？

確認前不進入逐頁草稿或 HTML 製作。
