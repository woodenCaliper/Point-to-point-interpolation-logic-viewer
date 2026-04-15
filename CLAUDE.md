# CLAUDE.md — Development Rules

## ドキュメント運用ルール（必須・毎回遵守）

### 2ファイルの役割分担

| ファイル | 内容 | 書き方 |
|---|---|---|
| `human requirement.md` | **「何を作るか」** — ユーザーの意図・要件・制約・受け入れ条件 | ユーザーの指示を受けてClaudeが書く。内容はユーザーの言葉を軽く校正した程度に留め、実装方針・技術的判断は一切書かない。 |
| `AI implementation instructions.md` | **「どう作るか」** — 実装方針・タスクリスト・状態管理設計など | `human requirement.md` を読んでClaudeが書く。実装の判断・設計はここに集約する。 |

### Claudeが守るべき手順

1. **ユーザーから指示を受けたとき**、その内容を `human requirement.md` に反映する（ユーザーの意図を整理・校正するだけ。実装の話は書かない）。
2. `human requirement.md` の内容を踏まえ、`AI implementation instructions.md` を更新する（実装方針・タスクをここに書く）。
3. 実装は `AI implementation instructions.md` に基づいて進める。
4. 実装完了後、`AI implementation instructions.md` のタスクリストを更新し、完了済みタスクにマークを付ける。

### NG行為

- `human requirement.md` に実装方針・技術的判断を書くこと。
- `AI implementation instructions.md` を更新せずに実装を進めること。
- `human requirement.md` に書かれた制約を `AI implementation instructions.md` で勝手に緩和・変更すること。
