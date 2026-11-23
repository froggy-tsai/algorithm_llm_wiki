# 演算法 LLM Wiki

這個專案以課堂教材為來源，逐步建立一份可追溯來源的演算法 Wiki，再以 Wiki 製作適合複習的互動式教學 HTML 簡報。專案也保留資料整理、簡報檢查與流程反思，供 TAICA「生成式 AI：文字與圖像生成的原理與實務」第十週作業使用。

## 專案原則

- 原始資料為使用者提供的五份課堂教材，放在 `sources/` 並保持不變。
- Wiki 與簡報只整理這些教材，不自行搜尋或補充外部資料。
- 演算法內容須保留必要的條件、步驟與嚴謹性，並盡可能標註來源檔名及投影片頁碼／標題。
- Wiki 依教材實際涵蓋的演算法類別與個別演算法整理。題目和解法放在相關演算法頁面中。
- 簡報製作為一份 HTML 檔，章節在同一份文件內以投影片／段落和內部導覽呈現；採可愛 Q 版視覺，並規劃逐步演示、可操作輸入及小測驗等互動學習方式。

## 目前進度

- 已 ingest：5 / 5 份教材。
- L1 涵蓋排序與演算法分析；L3 涵蓋分治法、搜尋、數值演算法、矩陣乘法及 VLSI 配置；L4a 涵蓋優先佇列、binary heap 與 heapsort；L4 涵蓋 quicksort 與 partition；L5 涵蓋比較排序下界、counting sort 與 radix sort。
- Wiki 索引和來源頁已建立，graph v1–v4 已留存，目前使用 v4。證據卡 v1、大綱 v1、逐頁草稿 v1–v2 已完成。原版簡報保留於 `presentation/index.html`；樹狀視角新版為 `presentation/index-v2.html`，包含比較決策樹、merge sort 遞迴樹、heap 二元樹與 quicksort 遞迴切分樹。新版已在 Chrome 抽查決策樹與 merge sort 樹的互動顯示；其餘互動和測驗仍待逐項確認，詳見執行紀錄。

## 資料夾導覽

```text
sources/                         原始課堂教材
wiki/
  index.md                       Wiki 導覽索引
  log.md                         按時間追加的維護紀錄
  concepts/                      共通概念
  data-structures/               資料結構
  algorithms/                    演算法分類與個別頁面
  sources/                       各份教材的摘要與來源索引
presentation/
  index.html                     單一 HTML 簡報（含投影片、樣式、互動與內部導覽）
assignment/
  graph-process/                 Graph 與版本化的證據卡、大綱和逐頁草稿
  run-log.md                     實際執行與檢查紀錄
  reflection.md                 實際執行後的反思
agent.md                         Wiki 維護規則與工作流程
```

## 建議工作順序

1. 將五份原始教材放入 `sources/`。
2. 依 `agent.md` 的 ingest 流程逐份整理教材，建立來源頁與 Wiki 內容，並更新索引及 log。
3. 依 `assignment/graph-process/workflow-v4.md` 執行教學設計；證據卡、大綱與逐頁草稿保存在該資料夾並以 v1、v2 等版本留存。原版簡報為 `presentation/index.html`，樹狀視角新版為 `presentation/index-v2.html`，兩者均可獨立開啟。
4. 檢查 Wiki 連結、來源標示、簡報內部導航、互動結果與內容正確性；依檢查結果修正並記錄。
5. 將實際流程、檢查結果與反思寫入 `assignment/`。執行紀錄和反思應來自實際操作，不預先編造。










