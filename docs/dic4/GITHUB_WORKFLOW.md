# DIC4｜獨立 GitHub + OpenSpec 工作流程

## 正式工作區

- **新 Repository：** `https://github.com/prometheans152/AIOT-DIC4-Overleaf-Paper`
- **本機：** `C:\Users\prometheans\Documents\AIOT_DIC4_OverleafPaper`
- **原產品 Repo：** `FreshMarketPriceForecastAgent`，僅作既有研究背景，不作此 DIC4 Repository 的 Git `origin`、fork 或 PR 目標。

## Goal

以 FMPA 的課堂提案與封存結果撰寫能在 Overleaf 開啟的 LaTeX 論文，保存可編輯的前後兩版與 2020 A–Z SOP 來源。數據忠實引用，不把尚未完成的真店 A/B 測試或 Domain Agent 新功能說成已驗證。

## Design

1. `paper/dic4/v1_before` 保存精簡對照初稿，`paper/dic4/v2_after` 保存修訂稿和真正由 Overleaf 編譯的 5 頁 PDF。
2. `docs/dic4/references` 保存使用者提供的兩份原始 PDF，並紀錄 SHA-256。
3. `docs/midterm/public_test_results.json` 是唯一與論文量化績效對應的封存依據；附原既有 `design.md`／`docs/dic3` 供查核。
4. `openspec/changes/dic4-overleaf-paper` 記錄規格與驗收情境。
5. GitHub 預設 `main` 是獨立專案，**不**合併回原產品 Repo。
6. Overleaf 使用者已登入，直接以 COS Browser 操作；**不需要 Overleaf MCP**。

## Tasks／驗收

1. 檢查使用者原始 PDF、LaTeX 與 ZIP 是否完整。
2. `python scripts/verify_dic4_paper.py` 重新比對原封存數據和引用。
3. `openspec validate dic4-overleaf-paper --strict --no-interactive` 檢查。
4. 以本 Repo 的 Git commit/push 發佈，查看 GitHub 檔案清單和原 PDF 尺寸／hash。
5. 原 Repo 上誤建 PR #2 已 **Closed**，沒有合併進產品 `main`。舊分支暫保留作備份。
6. 研究稿僅作課堂儲存與編輯；**不執行期刊、研討會、iLearning 正式投稿／繳交**。

`git add -A` 若在其他產品工作樹中執行可能夾帶舊改動，因此僅在本獨立 Repo 操作。不得將 credentials、cookie、`.env`、私人資料或未公開模型放進 Git。
