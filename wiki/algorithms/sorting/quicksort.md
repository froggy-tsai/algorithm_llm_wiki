# Quicksort（快速排序）

## 介紹

Quicksort 是由 C. A. R. Hoare 於 1962 年提出的分治排序演算法。它使用 partition 將陣列依 pivot 分成兩側，再遞迴排序兩個子陣列；合併步驟為 trivial。排序在原陣列中進行，教材將它與 insertion sort 一起列為 in-place 排序。

## Partition

教材的 `PARTITION(A,p,q)` 使用 `A[p]` 作為 pivot `x`：

```text
PARTITION(A, p, q)
    x = A[p]
    i = p
    for j = p + 1 to q
        if A[j] <= x
            i = i + 1
            exchange A[i] and A[j]
    exchange A[p] and A[i]
    return i
```

掃描期間，`A[p+1..i]` 收納不大於 pivot 的元素，`A[i+1..j−1]` 收納大於 pivot 的元素。最後把 pivot 放到索引 `i`，使左側元素 `≤ x`，右側元素 `≥ x`。Partition 的時間為 `O(n)`。

## Quicksort

```text
QUICKSORT(A, p, r)
    if p < r
        q = PARTITION(A, p, r)
        QUICKSORT(A, p, q − 1)
        QUICKSORT(A, q + 1, r)
```

初始呼叫為 `QUICKSORT(A, 1, n)`。Partition 回傳的 pivot 位置不再包含於後續兩個子問題。

## 時間分析

### 最壞情況

若輸入已排序或反向排序，而 pivot 每次取目前子陣列第一個元素，就會選到最小或最大值；其中一側子問題為空。遞迴式為：

`T(n)=T(0)+T(n−1)+Θ(n)`

Partition 每層花線性時間，遞迴深度達 `n`，所以總時間為 `Θ(n²)`。這個最壞情況不達到 comparison sort 的 `Ω(n lg n)` 下界階；下界背景見[比較排序的決策樹下界](../../concepts/comparison-sorting-lower-bound.md)。

### 平衡切分

若 partition 每次將陣列均勻切成兩半：

`T(n)=2T(n/2)+Θ(n)=Θ(n lg n)`

教材也分析固定 `1:9` 的切分，及 lucky/unlucky 交替的切分模式，指出這類近似平衡的遞迴仍可達 `Θ(n lg n)`。此處的 lucky/unlucky 為分析用的切分描述。

## Randomized quicksort

隨機化版本以隨機元素作 pivot。教材指出，執行時間不依賴輸入原有的排序順序，也不需假設輸入分布；分析由隨機數產生器造成的切分決定。

投影片假設輸入元素互異，並假設隨機選擇彼此獨立。若 pivot 產生 `k : n−k−1` 的切分，各切分機率為 `1/n`。定義指示隨機變數 `Xₖ` 表示是否產生該切分，則 `E[Xₖ]=1/n`。投影片建立期望執行時間遞迴式，並以代入法證明上界 `E[T(n)] ≤ a n lg n`（對適當常數 `a`），因此得到期望時間 `O(n lg n)`。

這段講義證明提供的是期望時間上界；不將其改寫為講義未證明的緊確界。隨機化不排除特定執行中出現不平衡切分；投影片著重於固定輸入下由隨機選擇決定切分結果。

## 重複元素

隨機化分析明確假設輸入元素互異。講義指出實務上有重複鍵時可採更好的 partitioning algorithms，但本份材料未提供其步驟或分析。本頁不補寫該變體。

## 教材中的實務觀察

最後一張投影片稱 quicksort 是通用排序演算法、常見情況下通常比 mergesort 快兩倍以上，且可透過程式碼調校受益，也能與 caching 和 virtual memory 配合。講義未列出具體硬體、資料分布或實驗條件，因此這些僅作為該課堂投影片的實務觀察，不視為普遍保證。

## 題目與解法

**排序題**：排序陣列 `A[1..n]`。Quicksort 以 partition 確定一個 pivot 的位置，使兩側元素分屬 pivot 兩邊，再遞迴排序兩側子陣列。教材示範的 partition 輸入為 `[6, 10, 13, 5, 8, 3, 2, 11]`，pivot 為第一個元素 `6`。

## 來源

- `L4_Quicksort.pdf`，投影片 2–18（演算法、partition、偽碼與分析前提）、19–26（最壞情況）、27–33（平衡與近似平衡切分）、34–46（隨機化及期望分析）、47（實務觀察）。

