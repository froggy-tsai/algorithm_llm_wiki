# L5 — Sorting Lower Bounds

## 來源資訊

- 檔案：[`L5_SortingLowerBounds.pdf`](../../sources/L5_SortingLowerBounds.pdf)
- 課堂標題：*Introduction to Algorithms — Lecture 5: Sorting Lower Bounds*
- 投影片日期：2024-02-19
- PDF 範圍：8 個講義頁面，含投影片 1–47。
- 定位慣例：引用數字為每張投影片左下角印出的投影片編號；講義每頁約排 6 張投影片。
- 附錄範圍：投影片 40–47 討論 Herman Hollerith、打孔卡與 radix sort 歷史；本 Wiki 保留範圍摘要，不另建歷史主題頁。

## 內容摘要

1. **比較排序下界與決策樹**（投影片 1–10）：以決策樹表示比較排序各種比較路徑；因 `n` 個互異元素有 `n!` 種排列，樹必須至少有 `n!` 個葉節點，得到高度 `Ω(n lg n)`。Heapsort 與 merge sort 因達到此階漸進時間而為 asymptotically optimal comparison sorts。
2. **Counting sort**（投影片 11–30）：對鍵值位於 `1..k` 的輸入計數、累積位置並穩定地填入輸出陣列；時間 `Θ(n+k)`，若 `k=O(n)` 則為線性時間。它不比較元素。
3. **Radix sort**（投影片 31–39）：由最低位往最高位逐趟排序，需每趟使用穩定排序；分析每個鍵值 `b` 位元、每趟 `r` 位元時的總時間，並以 `r≈lg n` 說明可能的線性時間條件。
4. **實務與歷史附錄**（投影片 39–47）：比較 radix sort、quicksort 的課堂實務觀察；附錄介紹打孔卡、Hollerith 設備與 radix sort 起源。

## 投影片主題對照

| 投影片 | 主題 |
|---|---|
| 1–10 | 比較排序決策樹及 `Ω(n lg n)` 下界 |
| 11–30 | Counting sort 偽碼、範例、穩定性與分析 |
| 31–39 | Radix sort、穩定性證明、基數選擇與效能 |
| 40–47 | 打孔卡與 Hollerith 歷史附錄 |

## 已整理到的 Wiki 頁面

- [比較排序的決策樹下界](../concepts/comparison-sorting-lower-bound.md)
- [Counting sort](../algorithms/sorting/counting-sort.md)
- [Radix sort](../algorithms/sorting/radix-sort.md)
- [Merge sort](../algorithms/sorting/merge-sort.md)
- [Heapsort](../algorithms/sorting/heapsort.md)
- [Quicksort](../algorithms/sorting/quicksort.md)

## 待確認／限制

- 下界推導針對 comparison sorts，並以元素互異時的 `n!` 種輸入排列計數。
- Counting sort 的線性時間依賴 `k=O(n)`；radix sort 的線性時間依賴位數、每趟基數及穩定輔助排序條件。
- PDF renderer 回報一個 xref 參照缺失並自動重建；文字可擷取，8 頁皆可渲染並已目視核對。
- 附錄的歷史文字引用投影片內所列來源；本 Wiki 不另作外部查證或延伸。
