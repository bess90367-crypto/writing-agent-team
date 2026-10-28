# Writing Agent Team

這是一套依照「寫信」專案長期使用習慣建立的 **主管制多 Agent 寫作系統**。

使用者只需要把需求交給 **Manager Agent**；Manager 會自行判斷收件者、訊息載體、行政情境與風險，再調用適合的專責 Agent，不需要使用者自己選 Agent。

## Team

- **Manager Agent**：唯一入口、需求判斷、路由、整合與最終輸出
- **Email Writer**：一般行政信、新信與回信
- **Instant Message Writer**：LINE、DM、群組訊息
- **Formal Admin Writer**：公文式文字、簽辦、正式行政措辭
- **Announcement Writer**：學生公告、表單、海報、網站短文案
- **Editor**：精簡、自然化、調整語氣、提供差異化版本
- **Critic**：寄出前檢查資訊、語氣、責任與下一步是否清楚

## Core behavior

這套系統目前學到的核心不是「固定模板」，而是一組可維護的寫作判斷：

- 自然、簡潔、完整，不寫成公文腔
- 有禮但避免過度卑微，也避免對老師或合作對象產生上對下感
- 回信不重複對方已知道的整段前情
- 背景、目前狀態、希望對方做什麼、期限盡量一次說清楚
- 學生規則與後果不能因為想寫得客氣而變模糊
- 對外協調避免強迫感
- 不加入使用者沒有打算執行的後續承諾
- 多版本必須真的有差異，而不是只換幾個同義詞

詳見：
- `knowledge/style-rules.md`
- `knowledge/recipient-rules.md`
- `knowledge/scenario-rules.md`
- `knowledge/work-domains.md`

## How routing works

```
User
  ↓
Manager
  ↓
Primary specialist
  ↓
Editor (when needed)
  ↓
Critic (when needed)
  ↓
Manager finalizes
```

規則見 `routing/routing-rules.md`，機器可讀設定見 `config/team.yaml`。

## Continuous learning

只要「寫信」專案後續出現新的可泛化偏好、修正意見、常見情境或失敗案例，就應依 `ops/incremental-learning.md` 主動更新：

1. 對應的 knowledge rule
2. 必要的 agent / routing rule
3. regression case
4. `CHANGELOG.md`

不是所有單次修字都要永久記住；只有穩定、可重複使用的規則才升級為長期知識。

## PDF / image learning

附件處理遵循 `ingestion/attachment-policy.md`：

**PDF / image → 可檢索文字 → 判斷一次性事實與可泛化規則 → 更新知識庫／測試**

不直接把看不懂的圖片或 PDF 當成 prompt 素材。

## Evaluation

`evals/` 目前包含：
- routing cases
- regression cases
- 評測原則

每次 durable rule 改動，都應確認沒有破壞舊有重要偏好。

## Automated maintenance

已建立**每小時自我優化檢查**與**每週一深度週檢**兩套長期排程，定期檢查：
- 最近專案對話是否出現新偏好
- 規則是否互相衝突
- 是否有重複或過度擴張的規則
- 是否缺少 regression test
- 是否需要更新 routing / examples / knowledge

排程與維護規則見 `ops/`。

## Version

Current version: **0.1.0**

See `CHANGELOG.md`.
