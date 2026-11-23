# Heapsort（堆積排序）

## 介紹

Heapsort 以 max-heap 排序陣列。max-heap 的根節點是目前最大元素；每輪把根與 heap 尾端交換，將尾端元素視為已排序，再縮小 heap 範圍並修復根節點可能造成的違規。

## 演算法流程

1. 將未排序陣列轉成 max-heap。
2. 取出根節點 `A[1]`（目前最大值）。
3. 交換 heap 尾端元素與 `A[1]`，最大值因此放到陣列末端。
4. 將 `heap-size` 減一，讓已排序尾端不再屬於 heap。
5. 對新的根呼叫 `MAX-HEAPIFY`，恢復 max-heap 性質。
6. 重複以上步驟，直到 heap 為空。

見 [Binary heap 與優先佇列](../../data-structures/binary-heap.md)了解 `MAX-HEAPIFY` 與建堆。

## 複雜度

- 建立 max-heap：`O(n)`。
- 排序階段：教材說明共進行 `n` 輪，每輪包含交換與 `MAX-HEAPIFY`，每輪為 `O(lg n)`。
- 整體時間：`O(n lg n)`。

以上保留教材提供的漸進上界記號。

## 教材示例

建堆示範輸入陣列：`[4, 1, 3, 2, 16, 9, 10, 14, 8, 7]`。教材接著逐輪示範將最大值交換到陣列尾端、縮小 heap 並呼叫 `MAX-HEAPIFY`。

## 題目與解法

**排序題**：將未排序陣列排列。解法是先建 max-heap，再反覆將最大值移至尚未排序區間的最後一格，直到整個陣列排序完成。本教材以建堆範例和逐輪圖示示範此流程，未提供額外獨立程式練習題。

## 來源

- `L4a_Heapsort.pdf`，投影片 16–26。
- 建堆細節及分析見[Binary heap 與優先佇列](../../data-structures/binary-heap.md)，來源為同份教材投影片 2–15。
