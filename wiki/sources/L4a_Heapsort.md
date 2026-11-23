# L4a — Heapsort

## 來源資訊

- 檔案：[`L4a_Heapsort.pdf`](../../sources/L4a_Heapsort.pdf)
- 課堂標題：*Introduction to Algorithms — Lecture 4: Heapsort*
- 投影片日期：2025-03-11
- PDF 範圍：5 頁橫式講義版，含投影片 1–26。
- 定位慣例：引用數字為每張投影片左下角印出的投影片編號，不是 PDF 實體頁碼。

## 內容摘要

1. **優先佇列**（投影片 2）：介紹 `insert`、`max`、`extract_max`、`increase_key` 操作，並假設 increase_key 的新值至少與舊值一樣大。
2. **Heap 表示法**（投影片 3–5）：以陣列表示 nearly complete binary tree，介紹 max-heap 性質、父子索引公式及 `build_max_heap`、`max_heapify`。
3. **Max-heapify**（投影片 6–10）：假設左右子樹已是 heaps，將違反性質的節點往下移；時間上界 `O(lg n)`。
4. **Build-max-heap**（投影片 11–15）：由 `⌊n/2⌋` 向上呼叫 max_heapify；雖然簡單估算可得到 `O(n lg n)`，依節點高度加總可證明更緊的 `O(n)` 上界。
5. **Heapsort**（投影片 16–26）：先建 max-heap，再將最大元素移到陣列尾端、縮小 heap、修復 root；總時間上界 `O(n lg n)`。

## 已整理到的 Wiki 頁面

- [Binary heap 與優先佇列](../data-structures/binary-heap.md)
- [Heapsort](../algorithms/sorting/heapsort.md)

## 待確認／限制

- 講義的複雜度以 `O` 上界表示；本 Wiki 不將其改寫成 Θ 緊確界。
- Heap 以 1 起始索引表示；程式語言中的 0 起始陣列轉換方式不在本講義範圍內。
- 本講義主要以圖示呈現 heapsort 演示；未提供獨立的程式練習題。
