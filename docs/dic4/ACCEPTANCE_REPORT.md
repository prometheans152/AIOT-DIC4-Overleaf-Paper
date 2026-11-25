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
| `paper/dic4/v2_after/` | 修訂版 LaTeX／BibTeX 與 2026-11-25 Overleaf 產生的 5 頁 PDF |
| `paper/dic4/v2_after_overleaf.zip` | 可重新匯入 Overleaf 的 LaTeX 專案包 |
| `docs/dic4/REVISION_COMPARISON.md` | 修改前與修改後差異說明 |
| `openspec/changes/dic4-overleaf-paper/` | OpenSpec proposal、design、specs、tasks |
| `docs/midterm/public_test_results.json` | 既有公開市場回測封存結果，不是本輪訓練產生 |
| `design.md`、`docs/dic3/DIC3_PROPOSAL_REFACTOR.md` | 供論文與 OpenSpec 對照的既有設計／提案參考，非新產品程式碼 |
| `docs/dic4/references/` | 使用者提供的 2 份 PDF 原檔，SHA-256 如下 |

| PDF | bytes | SHA-256 |
| --- | ---: | --- |
| `A2Z outline example(1).pdf` | 140798 | `777386D58818577471BB02067CD01B7B14D24DC55B497A6D667FEBDB2C207EF4` |
| `FMPA 專題簡報解析.pdf` | 196944 | `457A52540F5DC43D080C021408289B0A33458FA91570D78E69A4377958715FEC` |

原修訂稿 Overleaf PDF：238258 bytes、5 頁、SHA-256 `71A872F86BE2F4288AB7C5707626700DCFAB4604F27D9E999E3910A11F200B61`。先前已實際逐頁檢視，未見文字越界；第 5 頁為參考文獻。新 repo 本身不等於重新跑過模型或完成學術審稿。

## 驗收與限制

在 repo 根目錄可執行 `python scripts/verify_dic4_paper.py` 檢查引用、簡要 LaTeX 結構及封存 7／14 天評估數字；OpenSpec 以 `openspec validate dic4-overleaf-paper --strict --no-interactive` 驗證。實際執行結果以當次工具紀錄為準。

研究未驗證個別店家的 7／14 天預測精度、B 模式是否改善、消費者是否省錢；原 RF/HGB 在指定的公開市場 macro-F1 和相對變化 MAE 指標未贏對應簡單基線。PDF 解析文件的「完全符合」用語是該文件自身的評述，**不是本專案已獨立驗證所有教授評分規則的證據**。

## GitHub 發佈與原 Repo

DIC4 曾被誤放到 `FreshMarketPriceForecastAgent` 的 `dic4/overleaf-paper-20261125` 分支及 PR #2；使用者已澄清應**建立獨立 repo**。本 Repo 才是 DIC4 的正式版本來源；原 Repo 的 `main` 不因本次改動。最終 GitHub 推送／原 PR 收尾狀態需以線上確認為準。

**Overleaf MCP 省略**：依使用者授權，直接以 COS Browser 編輯、匯入與編譯；不連接不必要的第三方 MCP。正式投稿、iLearning 課程繳交皆未執行。
