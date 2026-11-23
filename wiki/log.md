# Wiki 維護紀錄

## [2026-11-22] ingest | L1 — Analysis of Algorithms

- 來源：`sources/L1_AnalysisOfAlgorithms-1.pdf`（使用者提供原始 PDF，保持未修改）。
- 範圍：PDF 9 頁，包含投影片 1–51 的講義版；以投影片上印的編號作為引用定位。
- 擷取並整理：演算法分析、排序問題、插入排序、執行時間與最好／平均／最壞情況、漸進分析與 Θ 記號、merge sort、合併已排序序列、遞迴式及遞迴樹。
- 建立：來源索引、3 篇概念頁、2 篇排序演算法頁，並更新 Wiki 索引。
- 檢查：核對文字擷取與 PDF 頁面影像；確認主要章節、示例步驟、遞迴樹和結論的投影片定位。PDF 每實體頁約排 6 張投影片，因此來源註記採投影片編號。
- 待辦：後續教材可能補充、修正或擴展相同主題；新增時保留各自來源並檢查差異。本次尚未製作 HTML 簡報或完成五份資料的整體 lint。

## [2026-11-22] ingest | L3 — Divide and Conquer

- 來源：`sources/L3_DivideAndConquer.pdf`（使用者提供原始 PDF，保持未修改）。
- 範圍：PDF 9 頁，包含投影片 1–54 的講義版；以投影片上印的編號作為引用定位。
- 整理主題：分治法、Master theorem、二分搜尋、快速冪、Fibonacci 計算、標準與分治矩陣乘法、Strassen 演算法、VLSI tree layout 與 H-tree embedding。
- 新增：分治法及 Master theorem 概念頁；搜尋、數值演算法、矩陣乘法與版面配置頁；來源摘要；並更新 merge sort、遞迴式、Wiki 索引及 README。
- 檢查：核對文字擷取與 9 頁 PDF 影像；確認演算法公式、Fibonacci 定義動畫後的最終形式、矩陣乘積公式、遞迴式與投影片編號。PDF 每實體頁排約 6 張投影片，因此來源註記採投影片編號。
- 限制：binary search 的未命中／重複元素規格、快速冪基底情況與 VLSI 完整幾何條件未在教材充分說明，均未自行補寫。Strassen 約 n≥32 的實務說法只保留為教材觀察。
- 狀態：已整理 2 / 5 份教材；尚未製作 HTML 簡報或進行全 Wiki lint。

## [2026-11-22] ingest | L4a — Heapsort

- 來源：`sources/L4a_Heapsort.pdf`（使用者提供原始 PDF，保持未修改）。
- 範圍：PDF 5 頁橫式講義版，包含投影片 1–26；引用採投影片印刷編號。
- 整理主題：priority queue 操作、max-heap 陣列表示、max_heapify、build_max_heap 的線性上界、heapsort 流程與總時間上界。
- 建立：binary heap／priority queue 資料結構頁、heapsort 排序演算法頁與來源摘要；更新 Wiki 索引及 README。
- 檢查：核對文字擷取和 5 頁 PDF 影像，確認索引公式、heapify 前提與偽碼、建堆分層加總、heapsort 範例流程及複雜度定位。
- 限制：沿用教材的 O 上界，不改寫成 Θ；陣列索引維持教材的 1 起始慣例。
- 狀態：已整理 3 / 5 份教材；尚未製作 HTML 簡報或完成全 Wiki lint。

## [2026-11-22] ingest | L4 — Quicksort

- 來源：`sources/L4_Quicksort.pdf`（使用者提供原始 PDF，保持未修改）。
- 範圍：PDF 8 頁，包含投影片 1–47 的講義版；來源註記採投影片印刷編號。
- 整理主題：quicksort 分治流程、線性 partition 子程序、最壞情況 Θ(n²)、平衡／近似平衡切分 Θ(n lg n)、randomized quicksort 期望上界 O(n lg n)。
- 建立：quicksort 演算法頁及來源摘要；更新 Wiki 索引和 README。
- 檢查：核對文字擷取與 8 頁 PDF 影像；確認 partition 偽碼、輸入排序示例、遞迴式、不同分析假設與投影片定位。
- 限制：randomized 分析的元素互異與隨機選擇獨立假設、duplicate-key 限制及講義所述實務比較均明確保留；未把期望上界 O(n lg n) 改寫為緊確界。
- 狀態：已整理 4 / 5 份教材；尚未製作 HTML 簡報或完成全 Wiki lint。

## [2026-11-22] ingest | L5 — Sorting Lower Bounds

- 來源：`sources/L5_SortingLowerBounds.pdf`（使用者提供原始 PDF，保持未修改）。
- 範圍：PDF 8 頁，含投影片 1–47；投影片 40–47 為打孔卡與 Hollerith 歷史附錄。
- 整理主題：比較排序決策樹下界、counting sort、穩定性、radix sort 及每趟位數／基數的時間分析。
- 建立：comparison-sort lower-bound 概念頁、counting sort 與 radix sort 演算法頁、來源摘要；並更新 quicksort 交叉連結、索引與 README。
- 檢查：擷取文字並檢視所有 8 頁 PDF 影像；renderer 對來源 PDF 回報 xref 參照缺失後成功重建，所有頁面均可讀取及渲染，公式與投影片位置已核對。
- 限制：下界只適用 comparison sorts；線性排序的結論附帶鍵值範圍、位數與穩定輔助排序條件。附錄史料保留在來源摘要，未延伸為 Wiki 主題頁。
- 狀態：已 ingest 5 / 5 份教材；簡報與作業 workflow／反思尚未建立或實際執行。

## [2026-11-22] query | 教學簡報範圍與證據整理（Graph v4）

- 查閱 Wiki 索引及排序定義、六種排序方法、比較排序下界和相關來源頁。
- 依使用者「快速複習各種演算法」及作業初學者教學目標，規劃「排序演算法：比較排序到線性時間排序」，串起排序問題、比較排序下界、insertion/merge/heap/quick/counting/radix sort；使用者確認大綱後繼續完成。
- 證據卡、大綱、逐頁草稿存於 `assignment/graph-process/`，按版本留存。以 Wiki 證據卡完成簡報主張核對，製作單檔 `presentation/index.html`。
- Chrome 抽查確認 HTML 可開啟、首頁及前兩頁可導覽，第一頁排序結果互動可運作。抽查尚未涵蓋所有互動和測驗，詳見 `assignment/run-log.md`。

## [2026-11-23] presentation | 樹狀視角互動版 v2

- 依使用者回饋保留原簡報 `presentation/index.html`，另製作 `presentation/index-v2.html`。
- 比較排序決策樹、merge sort 遞迴樹、heapsort 完全二元樹、quicksort 遞迴切分樹可視化；其他非樹結構演算法維持符合其流程的陣列／計數視圖。
- 新版逐頁視覺與互動變更記錄於 `assignment/graph-process/slide-draft-v2.md`；瀏覽器抽查與限制記錄於 `assignment/run-log.md`。
