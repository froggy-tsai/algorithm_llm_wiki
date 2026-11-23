# 演算法 Wiki 索引

本 Wiki 依已提供的課堂教材整理。分類會隨教材實際涵蓋內容擴充，所有頁面應標明其依據來源與投影片位置。

## 共通概念

- [演算法分析與執行時間](concepts/algorithm-analysis.md)：分析目的、輸入規模、最好／平均／最壞情況。
- [漸進分析與 Θ 記號](concepts/asymptotic-notation.md)：機器無關的成長率分析。
- [遞迴式與遞迴樹](concepts/recurrences-recursion-tree.md)：以遞迴樹分析 merge sort。
- [分治法](concepts/divide-and-conquer.md)：divide、conquer、combine 設計流程。
- [Master theorem](concepts/master-theorem.md)：分治遞迴式的三種分析情況。
- [比較排序的決策樹下界](concepts/comparison-sorting-lower-bound.md)：comparison sorts 的 Ω(n lg n) 最壞情況下界。

## 資料結構

- [Binary heap 與優先佇列](data-structures/binary-heap.md)：max-heap 性質、陣列表示、操作與建堆。

## 排序演算法

- [插入排序 (Insertion Sort)](algorithms/sorting/insertion-sort.md)：插入下一元素至已排序前綴；含教材範例與 Θ(n²) 分析。
- [合併排序 (Merge Sort)](algorithms/sorting/merge-sort.md)：遞迴排序兩半並合併；以遞迴樹與 Master theorem 分析。
- [Heapsort](algorithms/sorting/heapsort.md)：以 max-heap 反覆將最大元素放到陣列尾端。
- [Quicksort](algorithms/sorting/quicksort.md)：以 partition 分割並遞迴排序；含最壞及隨機化分析。
- [Counting sort](algorithms/sorting/counting-sort.md)：在有限鍵值範圍內計數並穩定輸出。
- [Radix sort](algorithms/sorting/radix-sort.md)：逐位穩定排序；時間依位數與每趟基數而定。

## 其他演算法

### 搜尋

- [二分搜尋 (Binary Search)](algorithms/searching/binary-search.md)：在已排序陣列中反覆保留一半搜尋範圍。

### 數值演算法

- [快速冪](algorithms/numeric/exponentiation.md)：以分治法將指數規模減半。
- [Fibonacci 計算方法](algorithms/numeric/fibonacci.md)：比較直接遞迴、由底向上與遞迴平方。

### 矩陣乘法

- [標準矩陣乘法](algorithms/matrix-multiplication/standard.md)：教材中的 Θ(n³) 基準方法。
- [分治矩陣乘法](algorithms/matrix-multiplication/divide-and-conquer.md)：8 次子矩陣乘法的直接分治版本。
- [Strassen 演算法](algorithms/matrix-multiplication/strassen.md)：以 7 次遞迴乘法計算區塊矩陣乘積。

### 版面配置

- [VLSI 樹狀配置與 H-tree](algorithms/layout/vlsi-tree-layout.md)：以遞迴關係分析樹嵌入網格的面積。

## 資料來源

- [L1 — Analysis of Algorithms](sources/L1_AnalysisOfAlgorithms-1.md)：演算法分析、插入排序、merge sort、漸進分析與遞迴樹。
- [L3 — Divide and Conquer](sources/L3_DivideAndConquer.md)：分治法、Master theorem、搜尋、數值演算法、矩陣乘法與 VLSI 配置。
- [L4a — Heapsort](sources/L4a_Heapsort.md)：優先佇列、heap、建堆與 heapsort。
- [L4 — Quicksort](sources/L4_Quicksort.md)：partition、quicksort 最壞情況與隨機化分析。
- [L5 — Sorting Lower Bounds](sources/L5_SortingLowerBounds.md)：比較排序下界、counting sort 與 radix sort。

## Ingest 狀態

- 已整理：5 / 5 份課堂教材。
- 原始教材 ingest 已完成；簡報、全 Wiki lint、實際 workflow 執行紀錄與反思仍待進行。
