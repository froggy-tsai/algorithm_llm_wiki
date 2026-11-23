# Binary heap（二元堆）與優先佇列

## 優先佇列

優先佇列是一種資料結構，維護一組帶有 key 的元素 `S`，並支援下列操作：

- `insert(S, x)`：將元素 `x` 插入 `S`。
- `max(S)`：回傳 `S` 中 key 最大的元素。
- `extract_max(S)`：回傳 key 最大的元素並將它從 `S` 移除。
- `increase_key(S, x, k)`：把元素 `x` 的 key 增加為 `k`；教材假設新值不小於原值。

若改用 min-heap，可類比定義最小值操作。

## Max-heap 性質與表示法

Max-heap 是一種優先佇列實作：以陣列儲存，視為一棵 nearly complete binary tree。每個節點的 key 大於或等於其子節點的 key。陣列索引從 1 開始時：

- 根節點在 `A[1]`。
- `parent(i) = ⌊i/2⌋`。
- `left(i) = 2i`。
- `right(i) = 2i+1`。

因此不需要樹節點指標；教材指出二元堆高度為 `O(lg n)`。Min-heap 的順序性質相反。

## `MAX-HEAPIFY`

### 前提與目的

假設以 `left(i)` 和 `right(i)` 為根的子樹已經是 max-heaps。若 `A[i]` 違反 max-heap 性質，就將它向下「trickle」到適當位置，使以 `i` 為根的子樹恢復為 max-heap。

### 偽碼

```text
MAX-HEAPIFY(A, i)
    l = left(i)
    r = right(i)
    if l <= heap-size(A) and A[l] > A[i]
        largest = l
    else
        largest = i
    if r <= heap-size(A) and A[r] > A[largest]
        largest = r
    if largest != i
        exchange A[i] and A[largest]
        MAX-HEAPIFY(A, largest)
```

教材給出的時間上界為 `O(lg n)`，與堆高成正比。

## `BUILD-MAX-HEAP`

將任意陣列轉成 max-heap：

```text
BUILD-MAX-HEAP(A)
    for i = ⌊n/2⌋ downto 1
        MAX-HEAPIFY(A, i)
```

從 `⌊n/2⌋` 開始，是因為其後的陣列元素都是葉節點，單一節點本身已是 heap。雖然單次 `MAX-HEAPIFY` 為 `O(lg n)`，建堆不能只用「節點數乘以最大堆高」估算。教材依節點到葉子的距離加總工作量：離葉 1 層的節點約 `n/4` 個，離葉 2 層約 `n/8` 個，依此類推，總和為 `O(n)`。

## 相關演算法

- [Heapsort](../algorithms/sorting/heapsort.md) 用 max-heap 反覆取出最大值，並將它放到陣列尾端。

## 來源

- `L4a_Heapsort.pdf`，投影片 2–15。
