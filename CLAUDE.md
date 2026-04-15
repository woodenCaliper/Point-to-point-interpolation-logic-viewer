# CLAUDE.md — Development Rules

## ドキュメント運用ルール（必須・毎回遵守）

### 2ファイル制

| ファイル | 書く人 | 内容 |
|---|---|---|
| `human requirement.md` | 人間 | 要件・指示・制約・受け入れ条件 |
| `AI implementation instructions.md` | Claude | 上記要件を実現するための実装方針・タスクリスト・状態管理設計など |

### Claudeが守るべき手順

1. **会話開始時・指示受領時**、まず `human requirement.md` を読む。
2. 要件または指示に変化があれば、`AI implementation instructions.md` を更新してから実装に入る。
3. `AI implementation instructions.md` には「どう実装するか」だけを書く。要件の転記・重複記載は最小限にする。
4. 実装完了後、`AI implementation instructions.md` のタスクリストを更新し、完了済みタスクにマークを付ける。
5. `human requirement.md` は人間が書くファイルなので、Claudeは**変更しない**。

### NG行為

- `human requirement.md` を Claudeが書き換えること。
- `AI implementation instructions.md` を更新せずに実装を進めること。
- `human requirement.md` に書かれた制約を `AI implementation instructions.md` で勝手に緩和・変更すること。
