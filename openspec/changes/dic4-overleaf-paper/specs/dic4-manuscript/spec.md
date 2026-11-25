# dic4-manuscript Specification

## ADDED Requirements

### Requirement: 可追溯修改前後論文草稿
DIC4 工作包 SHALL 具備兩個可編輯 LaTeX 版本，含 `main.tex` 及同目錄 `references.bib`，並提供具體修訂矩陣。修改前版本如於本輪重新建立，SHALL 明確註明並非歷史 Overleaf 修訂。
#### Scenario: 教授比較論文修改
- **WHEN** 查核 `v1_before` 和 `v2_after`
- **THEN** 兩版可分別開啟編輯且能對照 Abstract、Related Work、方法、結果和限制
- **AND** 修訂矩陣說明差異，不誤稱已向期刊投稿。

### Requirement: 報告數據需對封存結果一致
論文 SHALL 依原本 `public_test_results.json` 逐期限報告 test n、direction macro-F1、momentum macro-F1、relative-return MAE、no-change baseline 和上漲 recall；不得隱藏負向比較或以市場均價當店價真值。
#### Scenario: 核對量化結果
- **WHEN** 重新讀取 JSON 並對照論文表格
- **THEN** 7 日 n=2085、F1=0.4218<0.4226、MAE=0.0664>0.0436、up=16/158
- **AND** 14 日 n=1859、F1=0.4169<0.4306、MAE=0.0983>0.0748、up=23/268
- **AND** 所有 MAE 明示為市場相對變化誤差。

### Requirement: 研究狀態與文獻層級分離
論文 SHALL 有研究問題、來源、相關研究、方法、系統／Agent 邊界、公開市場實驗結果、前瞻真店驗證計畫、限制與結論。原研究只讀摘要/索引的文獻不可假稱全文實讀。
#### Scenario: 論文可供校閱
- **WHEN** 檢查修訂稿
- **THEN** RQ1 已有公開測試、RQ2 尚無店價到期、RQ3 尚缺全面 Agent 驗證分明
- **AND** B 的 alpha=0.3 為固定未訓練規則。

### Requirement: 第二節結尾必須具備 Article Summary Table
修訂稿 SHALL 在 Section II Related Work 最後、Section III Proposed Scheme／Architecture 之前提供八欄 Article Summary Table，欄位依序為 Ref.、Year、Problem、AI Method、Domain Knowledge、Dataset、Findings、Limitation。每筆文獻的證據層級 SHALL 明示，不得將只讀摘要、商店頁或課堂簡報當成完整實驗驗證。
#### Scenario: 查核章節與表格
- **WHEN** 檢查修訂稿 LaTeX 與 Overleaf PDF
- **THEN** 具備八欄、R01–R07 和 H17 共八筆相關研究或應用來源
- **AND** 使用 IEEEtran Conference 雙欄排版與 `table*`，表格在第二節結尾橫跨兩欄、先於第三節，不使用橫向頁面，且不與內文重疊

### Requirement: IEEE 雙欄成品剛好五頁
本輪修訂後 PDF SHALL 由 IEEEtran Conference 產出剛好五頁，保留第二節結尾的跨雙欄 Article Summary Table。延伸內容 SHALL 以原封存評估的分項分析、時間資料邊界與尚待驗證的同店配對測試為主，不可填入虛構實驗或藉字體放大灌頁。
#### Scenario: 驗證 PDF 與研究限制
- **WHEN** 使用 Overleaf 編譯並以 PDF 頁面檢查
- **THEN** PDF 共五頁，每頁有內容，版面不裁切，表格完整位於雙欄頁
- **AND** 新增之各蔬菜樣本數與 macro-F1 對應 `docs/midterm/public_test_results.json` 的 `by_crop`
- **AND** 不將未完成的真店驗證或 Agent 情境測試標為完成。
- **AND** 引用都能在 BibTeX 中找到，未核實的方法、結果或限制標示其資訊來源。
