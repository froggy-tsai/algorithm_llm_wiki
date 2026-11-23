# 快速冪 (Divide-and-Conquer Exponentiation)

## 題目

計算 `a^n`，其中 `n ∈ N`。教材指出，逐次相乘的 naive algorithm 時間為 `Θ(n)`。

## 分治演算法

利用指數減半：

- 若 `n` 為偶數：`a^n = a^(n/2) × a^(n/2)`。
- 若 `n` 為奇數：`a^n = a^((n−1)/2) × a^((n−1)/2) × a`。

教材給出的遞迴式為 `T(n) = T(n/2) + Θ(1)`，結論為 `Θ(lg n)`。教材投影片未列出完整偽碼或基底情況，本頁不自行補寫實作細節。

## 與分治法的關係

問題規模每次約減半，只遞迴計算一個較小的冪次，再以常數次乘法組合結果。設計框架見[分治法](../../concepts/divide-and-conquer.md)，遞迴式形式可見[Master theorem](../../concepts/master-theorem.md)。

## 來源

- `L3_DivideAndConquer.pdf`，投影片 16–18。
