# 標準矩陣乘法 (Standard Matrix Multiplication)

## 題目

給定兩個 `n × n` 矩陣 `A=[aᵢⱼ]` 和 `B=[bᵢⱼ]`，計算 `C=A×B`。元素由下式計算：

`cᵢⱼ = Σ(k=1..n) aᵢₖ bₖⱼ`

## 標準演算法

對每個列索引 `i`、欄索引 `j`，先將 `cᵢⱼ` 設為 0，再對 `k=1..n` 累加 `aᵢₖ × bₖⱼ`。

## 時間複雜度

教材給出 `Θ(n³)`。

## 比較

此頁作為[分治矩陣乘法](divide-and-conquer.md)與[Strassen 演算法](strassen.md)的比較基準。教材指出一般分治法仍為 `Θ(n³)`；Strassen 以較少的遞迴矩陣乘法降低漸進指數。

## 來源

- `L3_DivideAndConquer.pdf`，投影片 27–30、34。
