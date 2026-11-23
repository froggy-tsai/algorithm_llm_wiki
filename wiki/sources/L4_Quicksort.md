# L4 — Quicksort

## 來源資訊

- 檔案：[`L4_Quicksort.pdf`](../../sources/L4_Quicksort.pdf)
- 課堂標題：*Introduction to Algorithms — Lecture 4: Quicksort*
- 投影片日期：2024-02-19
- PDF 範圍：8 個講義頁面，含投影片 1–47。
- 定位慣例：引用數字為每張投影片左下角印出的投影片編號；講義每頁排約 6 張投影片。

## 內容摘要

1. **Quicksort 設計**（投影片 1–3）：描述其分治流程、原陣列內排序，以及 `PARTITION` 為線性時間關鍵子程序。
2. **Partition**（投影片 4–16）：以子陣列第一個元素為 pivot，線性掃描並交換元素，最後將 pivot 放在分割位置；示例輸入為 `[6, 10, 13, 5, 8, 3, 2, 11]`。
3. **Quicksort 偽碼與分析假設**（投影片 17–18）：partition 後遞迴排序 pivot 左右子陣列；分析假設輸入元素互異，重複鍵需其他 partition 方法。
4. **最壞情況**（投影片 19–26）：已排序或反向排序輸入可能令 pivot 總是最小或最大，產生空的一側及 `Θ(n²)` 時間。
5. **平衡與近似平衡切分**（投影片 27–33）：平衡切分得到 `Θ(n lg n)`；教材分析固定 `1:9` 及 lucky/unlucky 交錯切分仍可得到 `Θ(n lg n)`。
6. **Randomized quicksort**（投影片 34–46）：隨機選 pivot；在輸入元素互異及隨機選擇獨立的假設下，推導期望執行時間 `O(n lg n)` 上界。
7. **實務觀察**（投影片 47）：提出 quicksort 的常見速度及調校觀察，但未給實驗條件。

## 已整理到的 Wiki 頁面

- [Quicksort](../algorithms/sorting/quicksort.md)
- [Insertion sort](../algorithms/sorting/insertion-sort.md)
- [Merge sort](../algorithms/sorting/merge-sort.md)
- [Heapsort](../algorithms/sorting/heapsort.md)

## 待確認／限制

- 來源只提供一種 partition 偽碼：pivot 固定取 `A[p]`，條件為 `A[j] ≤ x`。
- 最壞情況分析假設該 pivot 規則遇到已排序或反向排序資料；隨機化分析則另採隨機 pivot、輸入元素互異及獨立隨機選擇的假設。
- 重複元素的替代 partition 方法未在投影片中說明。
- quicksort 與 mergesort 的實務速度比較未列測試環境，不作通用效能保證。
