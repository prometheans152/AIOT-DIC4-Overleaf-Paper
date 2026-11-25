# DIC4 獨立 Repository 交付驗收

更新：2026-11-25（Asia/Taipei）。**本專案只保存課堂研究草稿與文件，未向任何期刊、研討會或 iLearning 投稿／繳交。**

## 專案邊界

- 新 GitHub Repository：`https://github.com/prometheans152/AIOT-DIC4-Overleaf-Paper`。
- Windows 本機：`C:\Users\prometheans\Documents\AIOT_DIC4_OverleafPaper`。
- Overleaf 工作草稿：`https://www.overleaf.com/project/6b06bd77157dbfcfac3cf914`。
- 本 Repo 採獨立 Git 初始化，不從舊 `FreshMarketPriceForecastAgent` 的 Git 歷史建立分支。
- 不複製 ML 模型、服務設定、密鑰、私人店家紀錄，不執行部署與重訓。

## 正文與附件

| 成品 | 內容與狀態 |
| --- | --- |
| `paper/dic4/v1_before/` | 本輪產生的精簡論文初稿與 BibTeX，非歷史投稿檔 |
| `paper/dic4/v2_after/` | 修訂版 LaTeX／BibTeX 與 2026-11-25 Overleaf 產生的 7 頁 PDF；第 3 頁橫式 Article Summary Table |
| `paper/dic4/v2_after_overleaf.zip` | 可重新匯入 Overleaf 的 LaTeX 專案包 |
| `docs/dic4/REVISION_COMPARISON.md` | 修改前與修改後差異說明 |
| `openspec/changes/dic4-overleaf-paper/` | OpenSpec proposal、design、specs、tasks |
| `docs/midterm/public_test_results.json` | 既有公開市場回測封存結果，不是本輪訓練產生 |
| `design.md`、`docs/dic3/DIC3_PROPOSAL_REFACTOR.md` | 供論文與 OpenSpec 對照的既有設計／提案參考，非新產品程式碼 |
| Repo 根目錄：`A2Z outline example(1).pdf`、`FMPA 專題簡報解析.pdf` | 使用者提供的 2 份 PDF 原檔，SHA-256 如下 |

| PDF | bytes | SHA-256 |
| --- | ---: | --- |
| `A2Z outline example(1).pdf` | 140798 | `777386D58818577471BB02067CD01B7B14D24DC55B497A6D667FEBDB2C207EF4` |
| `FMPA 專題簡報解析.pdf` | 196944 | `457A52540F5DC43D080C021408289B0A33458FA91570D78E69A4377958715FEC` |

最新 Overleaf PDF：304680 bytes、7 頁、SHA-256 `54010327F04990AB20E495A485A000B1AE7E10C11BF90A464D60B5B12728E9A5`。第 3 頁橫式 Article Summary Table 位於第二節結尾，包含八欄、八筆原 DIC3 文獻整理；編譯完成（0 errors, 0 warnings），已檢查文字不超出 PDF 媒體框，且第 4 頁才開始第三節。此 PDF 不代表新模型實驗或正式投稿。

## 驗收與限制

在 repo 根目錄可執行 `python scripts/verify_dic4_paper.py` 檢查引用、簡要 LaTeX 結構及封存 7／14 天評估數字；OpenSpec 以 `openspec validate dic4-overleaf-paper --strict --no-interactive` 驗證。實際執行結果以當次工具紀錄為準。

研究未驗證個別店家的 7／14 天預測精度、B 模式是否改善、消費者是否省錢；原 RF/HGB 在指定的公開市場 macro-F1 和相對變化 MAE 指標未贏對應簡單基線。PDF 解析文件的「完全符合」用語是該文件自身的評述，**不是本專案已獨立驗證所有教授評分規則的證據**。

## GitHub 發佈與原 Repo

DIC4 曾被誤放到 `FreshMarketPriceForecastAgent` 的 `dic4/overleaf-paper-20261125` 分支及 PR #2；使用者已澄清應**建立獨立 repo**。

- 2026-11-25 已新建 `prometheans152/AIOT-DIC4-Overleaf-Paper`（與原產品 Repo 完全獨立），以新 `main` 推送 **27 個檔案**，首個 Commit：`3a1750cca8cc8ee4d9afc7fcac8121e5191c6272`。
- 已驗證 GitHub 遠端 `main` SHA 與本機相同；GitHub 線上檔案樹實際可見兩份 PDF。原檔大小與上方 SHA-256 均與本機來源一致。
- 原產品 Repo 的 [PR #2](https://github.com/prometheans152/FreshMarketPriceForecastAgent/pull/2) **已關閉（Closed）且未合併**；原產品 `main` 未因此修改。舊 DIC4 分支仍保留作可還原備份，不再作本次交付來源。

**Overleaf MCP 省略**：依使用者授權，直接以 COS Browser 編輯、匯入與編譯；不連接不必要的第三方 MCP。正式投稿、iLearning 課程繳交皆未執行。
