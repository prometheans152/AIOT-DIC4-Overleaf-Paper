# AIoT DIC4｜Overleaf 論文草稿與 OpenSpec

本 Repository 是 **DIC4 課堂論文文件獨立專案**，不是 FreshMarketPriceForecastAgent 的產品程式碼 Repository，沒有執行訓練、部署或正式投稿。

**GitHub：** https://github.com/prometheans152/AIOT-DIC4-Overleaf-Paper  
**Overleaf（已建立並編譯）：** https://www.overleaf.com/project/6b06bd77157dbfcfac3cf914

## 內容

| 路徑 | 說明 |
| --- | --- |
| `paper/dic4/v1_before/` | 2026-11-25 本輪重建的精簡論文初稿；非歷史投稿版本 |
| `paper/dic4/v2_after/` | 修改後 IEEE Conference 雙欄 LaTeX／BibTeX 與已由 Overleaf 編譯的 4 頁 PDF；Section II 結尾的 Article Summary Table 橫跨雙欄 |
| `paper/dic4/v2_after_overleaf.zip` | 可直接匯入 Overleaf 的四檔原始碼 ZIP（含 before 版本） |
| `docs/dic4/REVISION_COMPARISON.md` | 修改前／後對照 |
| `FMPA 專題簡報解析.pdf`（Repo 根目錄） | 使用者提供的 FMPA 簡報解析原始 PDF（2 頁） |
| `A2Z outline example(1).pdf`（Repo 根目錄） | 使用者提供的 2020 A–Z SOP 大綱原始 PDF（1 頁） |
| `docs/midterm/public_test_results.json` | 論文所引用原專題的封存公開市場實驗數字（未重訓） |
| `design.md`、`docs/dic3/DIC3_PROPOSAL_REFACTOR.md` | 原有設計與 DIC3 提案的唯讀參考副本（無產品程式） |
| `openspec/changes/dic4-overleaf-paper/` | OpenSpec proposal / design / specs / tasks |
| `scripts/verify_dic4_paper.py` | 不需額外 Python 套件的論文結構、引用、封存數值檢查 |
| `docs/dic4/ACCEPTANCE_REPORT.md` | 本獨立 Repository 的交付驗證紀錄 |

## 重新驗證

在本 Repo 根目錄執行：

```powershell
python scripts/verify_dic4_paper.py
```

要修改論文，可以在 Overleaf 編輯既有專案，或由 Overleaf 首頁的 **Create a new project → Existing project (.zip)** 匯入 `paper/dic4/v2_after_overleaf.zip`。以 pdfLaTeX 編譯；報告中已保存成功編譯的 PDF 副本。

本 Repository 的 OpenSpec 採 `spec-driven`；如安裝 `@fission-ai/openspec` CLI，可執行：

```powershell
openspec validate dic4-overleaf-paper --strict --no-interactive
```

## 實驗與學術範圍

原公開市場測試的 7／14 天方向 macro-F1 分別 0.4218／0.4169，未勝動量基線 0.4226／0.4306；相對變化 MAE 也未勝不變價基線。資料不包含同店同規格的未來個別店家價格，因此 **A/B 模式對店家的效益尚未經實證驗證**。各項結果不得宣稱成已投稿或已發表研究。

**狀態：課堂論文草稿；未正式投稿、未提交 iLearning；不需 Overleaf MCP。** 參考文獻中部分英文標題是工作譯名，正式發表前仍須校對原始書目。
